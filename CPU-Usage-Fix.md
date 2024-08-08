# 100% CPU usage after Windows update. How to Fix this issue by the below steps.

#### Run the following two commands, which set the IDLEDISABLE setting back to "0" and then re-applies the power management configuration.

#### Open (Admin) CMD window

#### First switch to:

```sh
C:\WINDOWS\system32>
```

#### Copy this string and hit enter:

```sh
PowerCfg /SETACVALUEINDEX SCHEME_CURRENT SUB_PROCESSOR IDLEDISABLE 000
```

#### Then copy this string and hit enter:

```sh
PowerCfg /SETACTIVE SCHEME_CURRENT
```

#### DONE! The 100% CPU issue is gone showing a real percentage load.
