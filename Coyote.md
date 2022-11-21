# Coyote Data Transfer
This installation contains a small container that can be used to handle data exchanges between different components of the monitoring system. Coyote is a Read-Transform-Write (RTW) toolkit that allows you to read data from some source, transform it then write it a destination. It allows you to read data and send it to Prometheus, read data from Alertmanager and send it to other systems like messaging systems, and perform a variety of other integration tasks.

## Alert Manager
The Alert Manager is configured to send all alerts to the "webhook" receiver, which is a web service in Coyote on port 9080. The Coyote configuration contains a job that listens to port 9080 and transforms the data it receives then writes it to the console. Another writer can be enabled to write the alert to a Webex channel.

## Metrics Collection

