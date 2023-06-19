# Linux Cluster Monitoring Agent

# Introduction
(about 100-150 words)
Discuss the design of the project. What does this project/product do? Who are the users? What are the technologies you have used? (e.g. bash, docker, git, etc..)
The Linux Cluster Monitoring Agent as the name indicates monitors the usage of the hardware by the user. The program runs in a Docker container where a psql instance has been created.

# Quick Start
- Start a psql instance using psql_docker.sh
- Create tables using ddl.sql
- Insert hardware specs data into the DB using host_info.sh
- Insert hardware usage data into the DB using host_usage.sh
- Crontab setup

# Implementation
Discuss how you implement the project.
## Architecture
![Cluster Diagram](assets/linux_monitoring_agent.png)

## Scripts
Shell script description and usage (use markdown code block for script usage)
- psql_docker.sh : create/start/stop the docker container and provision a psql instance. Usage : `./scripts/psql_docker.sh`
- host_info.sh : retrieves the information of the hardware and insert it a postgres table inside the `host_agent` database
- host_usage.sh : retrieves the
- crontab
- queries.sql (describe what business problem you are trying to resolve)

## Database Modeling
Describe the schema of each table using markdown table syntax (do not put any sql code)
- `host_info`
- `host_usage`

# Test
How did you test your bash scripts DDL? What was the result?

# Deployment
How did you deploy your app? (e.g. Github, crontab, docker)

# Improvements
Write at least three things you want to improve
e.g.
- handle hardware updates
- blah
- blah
