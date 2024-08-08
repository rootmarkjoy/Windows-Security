# 100% cpu usage after windows update.

Run the following two commands, which sets the IDLEDISABLE setting back to "0" and then re-applies the power management configuration.

Open (Admin) CMD window

Copy this string and hit enter:

``sh
PowerCfg /SETACVALUEINDEX SCHEME_CURRENT SUB_PROCESSOR IDLEDISABLE 000
```

Then copy this string and hit enter:

``sh
PowerCfg /SETACTIVE SCHEME_CURRENT
```

DONE! 100% CPU issue gone showing real percentage load
