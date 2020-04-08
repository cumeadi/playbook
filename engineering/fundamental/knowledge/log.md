## Logs

**Treat logs as event streams**. Logs are the stream of aggregated, time-ordered events collected from the output streams of all running processes and backing services.

Services should never concern themselves with routing or storing logs. Instead, apps should be as agnostic as possible as to not depend on any other system or process. Then our app should just put logs in stdout and if we want to collect and ship them other processes/apps should be in charge of that.

- In development, the developer will view this stream in the foreground of their terminal to observe the app’s behavior.
- In staging or production deploys, each process’ stream will be captured by the execution environment, collated together with all other streams from the app, and routed to one or more final destinations for viewing and long-term archival.

The event stream for an app can be routed to a file, or watched via realtime tail in a terminal. Most significantly, the stream can be sent to a log indexing and analysis system such as Splunk, or a general-purpose data warehousing system such as Hadoop/Hive. These systems allow for great power and flexibility for introspecting an app’s behavior over time, including:

- Finding specific events in the past.
- Large-scale graphing of trends (such as requests per minute).
- Active alerting according to user-defined heuristics (such as an alert when the quantity of errors per minute exceeds a certain threshold).
