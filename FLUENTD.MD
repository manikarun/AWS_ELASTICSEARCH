INSTALLING FLUENTD IN UBUNTU_BIONIC in Apache2

1.For Ubuntu Bionic,
```
curl -L https://toolbelt.treasuredata.com/sh/install-ubuntu-bionic-td-agent3.sh | sh
 ```
2.Add the configuration file td-agent.conf in /etc/td-agent/

3.Enable Apache2 SSL module
```
sudo a2enmod ssl
 ```

4.Launch Daemon,
```
sudo systemctl start td-agent.service
 ```
5. Collecting the daemon logs
```
sudo td-agent -c /etc/td-agent/td-agent.conf
 ```
6.monitor the logs in elatic search from kibana dashboard