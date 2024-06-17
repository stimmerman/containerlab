# AAA Lab

Can login with:
 - admin:admin
   - privilege 15, no limits
 - engineer:engineer
   - can't do `switchport trunk allowed vlan x` as demo for protecting from cli mistakes.

## Configuration sessions

```
rtr1#configure session aaa-1111                      # Start new config session with ticket number
rtr1(config-s-aaa-1111)#

  <- do changes ->

rtr1(config-s-aaa-1111)# show session-config diffs   # compare changes with running-config

rtr1(config-s-aaa-1111)# commit                      # no timer
rtr1(config-s-aaa-1111)# commit timer 00:10:00       # needs to be confirmed withing 10 minutes
```

- Show past configuration and pending sessions: `show configuration sessions detail`
- Show diff between last checkpoint and running config: `diff checkpoint:ckp-20240616-5 running-config`

