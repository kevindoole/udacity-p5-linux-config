# Udacity Project 5 -- Linux server config
This project is nothing more than a readme file with some details for a project
I have completed for the Udacity Full Stack Developer Nanodegree.

## Server details
- SSH access: 52.37.170.233:2200
- Hosted application: http://ec2-52-37-170-233.us-west-2.compute.amazonaws.com/

## Configuration changes
- An account called `grader` was added, and given sudo privilege.
- Remote root login is disabled.
- Only key-based auth is allowed.
- All currently installed packages have been updated.
- SSH port was set to 2200
- UFW is configured to only allow incoming connections for SSH (port 2200),
HTTP (port 80), and NTP (port 123).
- Local timezone was set to UTC.
- Apache and mod_wsgi installed.
- Apache configured to not serve indexes. Catalog application is served outside
the web root, so people can't just arbitrarily browse source files and git repo.
- PostgreSQL installed. Only the catalog user can access the catalog database.
Remote connections are not allowed.
- Installed git.

## 3rd Party software
- fail2ban is installed to ban users after failed login attempts, among other
things
- cron-apt is installed to check for software updates automatically every day
at 4am
- newrelic-agent is installed to monitor server status, in order to notify
me if anything is out of the ordinary
