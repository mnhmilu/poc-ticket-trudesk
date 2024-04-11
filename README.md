# poc-ticket-trudesk

ticketing system 

1. For AWS EC2 choose ***Ubuntu 20.04*** as per documentation, others may not work
2. Give enough volume space ( 30 GB min)
3. `curl -L -s https://storage.trudesk.io/install/ubuntu-1.2.sh | sudo bash` run 
4. In the first attempt elastic search , MongoDB installation will be successful but trudesk with Pm2 installation will show in progress (not started)
5. Wait for a while and reboot the system
6. Run script again, select n for mongo and Elasticsearch but select Y for Trudesk, trudesk will install successfully along with PM2
7. Check `sudo pm2 monit` or `sudo pm2 list` to see the process



## Troubleshoot

To get all service list in ubuntu use `systemctl list-units --type=service`
`

Suddenly application stopped reason was full disk space 

To check disk space use `df -h`

To check mongo service configuraiton info `sudo systemctl status mongod`

use `cat /etc/mongod.conf` to check mongodb configuration and log location 

use `journalctl -u mongod.service` to check error of mongod service error

To get mongod conf and other info use `systemctl show -p FragmentPath mongod`

now use `cat /lib/systemd/system/mongod.service` to view service details 



Do not use docker-compose as it is not stable 
`

## References

[Trudesk Documentation](https://docs.trudesk.io/v1.2/getting-started/deployment/docker-deployment)
