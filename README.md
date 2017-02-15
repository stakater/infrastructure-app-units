# Application Units for Stakater infrastructure applications

This repo contains different systemd unit files for infrastruction applications.

If any systemd unit has consul templates in  `infrastructure-app-units/<app_name>/consul-templates`, place those templates in `/admiral-config/<app_name>/consul-templates/`, before starting the unit


###Note:
Instance private IP is initialized by
`IPV4=$(curl http://169.254.169.254/latest/meta-data/local-ipv4)`
in some unit files due to the "Multiple IP issue": http://serverfault.com/questions/831542/multiple-ips-automatically-getting-attached-to-core-os-instance-on-ec2

Ideally, private IP of the instance should be fetched by `hostname -i` command, instead of using AWS meta-data API.
