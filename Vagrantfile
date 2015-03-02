# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "ohmage/ubuntu-14.04"
  config.vm.network "private_network", ip: "192.168.33.100"
  config.vm.hostname = "ohmage"
  config.vm.synced_folder "webapps/", "/var/lib/tomcat7/webapps", 
   owner: "tomcat7", group: "tomcat7" 

end