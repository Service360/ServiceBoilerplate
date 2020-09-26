# Post-mortem reports

Every service will fail sooner or later. Every failure is a learning
opportunity and this opportunity should not be missed. Every 
significant/customer-impacting failure should be documented here in 
order for the future maintainers of the service to learn.

Post mortem file should be named YYYY-MM-DD-<optional additional mnemonics>.md

Currently Service360 does not parse post-mortems nor it does any assumptions on its contents.

Though we can recommend to check some sources to get an idea on 
what good post-mortem means:
- Short and simple - [PagerDuty template](https://response.pagerduty.com/after/post_mortem_template/)
- In-depth and comprehensive - [Atlassian Incident Handbook](https://www.atlassian.com/incident-management/handbook/postmortems)

## Risk alert

If this folder is missing (or contains only boilerplate code, 
see DELETEME.md) Service360 will raise a LOW level alert.

Service360 does not analyze or make any assumptions on the contents 
of this directory. 
