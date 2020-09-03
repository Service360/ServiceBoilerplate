# Service audit DD.MM.YYYY

(Audit file should be named YYYY-MM-DD.md, for example: 2020-11-29.md)

Auditor: Name of the person who did an audit

Short audit summary goes here. Couple of sentences about overall
state of the service is enough.

## Checks

### Basic

- [ ] Previous service audit results are checked and planned actions 
are complete (or reassessed and transferred to this audit)
- [ ] Service passport is up to date (description, owner, state, tech, etc)
- [ ] Service dependencies (deps.s360.puml) are up to date
- [ ] Service release/rollback documentation is tested
- [ ] Service development documentation is tested
- [ ] Service how-to documentation is reviewed
- [ ] Service monitoring documentation is reviewed
- [ ] Service api documentation is reviewed
- [ ] Service360 detected risk level is at expected level

### Extended

- [ ] Disaster recovery scenario is tested
- [ ] Alerting is tested
- [ ] Service running costs are reviewed
- [ ] Service security is assessed
- [ ] Service architecture is assessed
- [ ] Code quality is assessed (test coverage, quality control 
tools, etc)

## Results

### Actions taken

Here goes log of the immediate actions taken during the audit.

For example:

- Added NewAwesomeService dependency
- Introduced how-to-manually-create-usage-report doc
- Removed Python2 from Tech list 

### Deficiencies found/Actions planned

List of deficiencies found and/or planned actions to fix those.

For example:

- CRITICAL. DB backups are not done since 160 days ago. Ticket SRV-321.
- MEDIUM. Free disk space alert is missing. Ticket SRV-322.
- MEDIUM. Shared team SSH key is used for the access. Ticket SRV-323
- LOW. Test environment creation documentation is missing. Ticket SRV-324.

### Kudos

Use this section to highlight interesting findings made during an
audit which might be helpful for other services/worth platform-wide
adoption.

For example:

- CONVENIENCE. Makefile command `make init` used to install/initialize service 
tooling needed for the development setup.
- TOOLING. Dead letter queue processing tool is introduced for semi-automated
DLQ processing