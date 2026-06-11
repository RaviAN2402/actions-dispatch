# actions-dispatch

Exact-time dispatcher for scheduled workflows in another repository.

GitHub's cron can start scheduled runs hours late at congested times. This
repo's workflow wakes early on staggered crons, sleeps until the exact target
time, then fires `workflow_dispatch` at the configured repository so its run
starts on time.

All configuration lives in repository secrets (`DISPATCH_TOKEN`,
`DISPATCH_CONFIG`) — nothing target-specific is committed here.
