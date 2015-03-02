# ohmage-vagrant

The fastest way to get testing and developing against ohmage! This is a vagrant box pre-configured to be running the latest stable version of ohmage the second you turn it on.  Obviously, some assumptions have been made about the deployment, so it should never be used in production.

It is based on the [ohmage chef cookbook](https://github.com/stevenolen/chef-ohmage) and the base box should be updated and become more feature-filled as that cookbook becomes more generic!

Below is a list of the installed software and a quick little guide to getting started!

## Getting Started

Simple as pie, right?

  * Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
  * Install [Vagrant](https://vagrantup.com)
  * Clone this repository, `cd` to it.
  * type `vagrant up`
  * Access your ohmage installation from your system at `192.168.33.100`.

## Installed Packages

Here are the installed packages:

  * Java (namely openjdk-7-jre-headless)
  * Tomcat 7
  * MySQL 5.5
  * nginx

And some information about what is doing what:

  * Tomcat7 is serving the ohmage 2.16 webapp on port `8080`
  * nginx is serving our various static frontends (stored at `/var/www`) on port `80` (and also proxying traffic from `/app` to tomcat7)
  * MySQL is configured to have a single db called `ohmage` with a user `ohmage` and password `pleasechangeme`
  * Visting `192.168.33.100` will allow you to log in, done with the initial info: `ohmage.admin` and password `ohmage.passwd`

## A few more quick notes!

  * You'll need to change the IP address the survey_tool points to if you opt not to use the private network address 192.168.33.100. You can do this by editing `/var/www/webapps/survey/js/config/ConfigManager.js`.

  Thanks, and have fun!
