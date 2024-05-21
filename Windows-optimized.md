Windows Server 2008/2012
IIS 7/8


#### Compression
HTTP compression lets you make more efficient use of bandwidth and enhances the performance of sites and applications. You can configure HTTP compression for both static and dynamic sites.
For more information about how to configure compression, see Configuring HTTP Compression in IIS 7.

#### Output Caching
Output caching allows you to manage output caching rules and to control the caching of served content. In IIS Manager, you can create caching rules, edit existing caching rules, and configure output cache settings.
For more information about configuring output caching, see Configuring Output Caching in IIS 7.

#### Enabled ASP Feature in IIS
This enables doing further settings like Threads per processor limit etc.

#### Threads per Processor limit
This setting was by default set to 25, according to the load you may extended it to 100.

#### Queue Length Property – Value
 is 3000 by default, but now we have set it 400 because this property  is supposed to be 4*Thread Per Processor hence coming out to be 400.

#### Max Pool Threads 
This setting specifies the number of pool threads to create per processor. This entry was not there we made this entry at HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\ with a value of 20.

#### Process Model (ASP.NET)
We can enabled the process model element and configured it to the following values in machine config
Max Worker Thread – 100
Max I/O Threads – 100
Min Worker Thread – 50

#### HTTP-Runtime element

We have made some changes in this element also:
minFreeThreads – 352 (88 * N ) where N is no of CPUs (4)
minLocalRequestFreeThreads – 304 (76*N)

#### Connection Pool Changes for SQL Server
connection time-out was by default set to 3600 sec which is a very high value and not recommended because in case of high load when all pools will be used by the pool connection there will be no pool available ultimately. The recommended value is 15 but we have set it to 30. And we have also increased the pool size to 300.
