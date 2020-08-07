# Monitoring

This folder should contain documentation on the service health 
monitoring measures/alerts: what kind of monitoring is present,
what triggers alerts, how a person should react on the alert.

It is recommended to create a separate file per monitored case.
One file can contain a multiple alerts. Though if the amount of alerts 
is low then putting them all in the README.md might make sense.

## Examples

Examples below illustrate just **minimal** useful documentation.
Try to keep documentation as concise as possible. Do not overload
it with unnecessary details.

### File ServiceIsDown.md

```markdown
# ServiceIsDown

Check if service is alive

## Alerts

### /ping endpoint is reachable

- Measure: Once 30 seconds /ping endpoint is invoked. HTTP 200 is expected.   
- Trigger: 3 failures in a row

#### Mitigation

- check logs at "https://log-location"
- act accordingly 
```

### File QueueProcessingIssues.md

```markdown
# QueueProcessingIssues

Check if queue processing goes as normal or if there are any issues

## Alerts

### There are messages in DLQ 

- Measure: > 0 messages are in DLQ
- Trigger: one failure

#### Mitigation 

- check logs at "https://log-location"
- act accordingly 

### Message processing is slow

- Measure: oldest message age
- Trigger: if oldest message age in the queue is > 360 seconds

#### Mitigation

- Check queue size at https://...
- Check for possible cues on why queue is growing in the logs https://...
- Increase amount of message processors (see "runbooks/how-to-change-amount-of-processors.md") 
```

###

## Risk alert

If this folder is missing (or contains only boilerplate code, 
see DELETEME.md) Service360 will raise a LOW level alert.

Service360 does not analyze the content of the directory.