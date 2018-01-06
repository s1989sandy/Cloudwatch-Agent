# Cloudwatch-Agent
[general]
state_file = /var/awslogs/state/agent-state  
 
[/var/log/messages]
file = /var/log/messages
log_group_name = /var/log/messages
log_stream_name = {instance_id}
datetime_format = %b %d %H:%M:%S


Installation:
ADD IAM role to the instance
sudo yum update -y
sudo yum install -y awslogs
/etc/awslogs/awslogs.conf
sudo service awslogs start

Default config file location is:
/etc/awslogs/awslogs.conf
If we need to specify the user defined config file location
logging_config_file = /var/vcap/jobs/awslogs/config/logging.conf
