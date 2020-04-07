## Backing services

Backing services (or infrastructure services) are datastores (such as MySQL or PostgreSQL), messaging/queueing systems (such as RabbitMQ or Beanstalkd), SMTP services for outbound email (such as Postfix), and caching systems (such as Memcached).

**Backing services should be treated as attached resources.**

The code for a twelve-factor app makes no distinction between local and third party services. To the app, both are attached resources, accessed via a URL or other locator/credentials stored in the config. A deploy of the twelve-factor app should be able to swap out a local MySQL database with one managed by a third party (such as Amazon RDS) without any changes to the app’s code.

We use environment variables to configure backing services (database for example), so we can easily change them.
