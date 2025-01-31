PHP Server Monitor NG
==================

.. image:: https://badges.gitter.im/Join%20Chat.svg
   :alt: Join the chat at https://gitter.im/erickrf/nlpnet
   :target: https://gitter.im/phpservermon/phpservermon
.. image:: https://cdn.huntr.dev/huntr_security_badge_mono.svg
   :alt: huntr
   :target: https://huntr.dev
Version 3.6.0.beta2

Forked from https://github.com/phpservermon/phpservermon 

## TODO :

* make php8 work
* documentation/wiki
* push new releas
* docker images

PHP Server Monitor is a script that checks whether your websites and servers are up and running.
It comes with a web based user interface where you can manage your services and websites,
and you can manage users for each server with a mobile number and email address.


Features:
---------

* Monitor services and websites (see below).
* Email, SMS, Discord, Pushover, Telegram and Jabber notifications.
* View history graphs of uptime and latency.
* User authentication with 2 levels (administrator and regular user).
* Logs of connection errors, outgoing emails and text messages.
* Easy cronjob implementation to automatically check your servers.

There are two different ways to monitor a server:

* Service

  A connection will be made to the entered ip or domain, on the given port.
  This way you can check if certain services on your machine are still running.
  To check your IMAP service for example, enter port 143.

* Website

  You can enter a link to a website, it will then use cURL to open the website and check the HTTP status code.
  If the HTTP status code is in the 4xx/5xx, it means an error occurred and the website is not accessible to the public.
  You can also set a regular expression to match for content on the page itself.
  If the regular expression returns no matches, the website is considered down.
  In both cases the script will return a "status offline", and will start sending out notifications.

Each server has its own settings regarding notification.
You can choose for email, text message (SMS), Pushover.net, Telegram and Jabber notifications.
The following SMS gateways are currently available:

* Clickatell - <https://www.clickatell.com>
* Inetworx - <https://www.inetworx.ch>
* Messagebird - <https://www.messagebird.com>
* Mosms - <https://www.mosms.com>
* Smsglobal - <https://smsglobal.com>
* SMSit - <https://www.smsit.dk>
* Spryng - <https://www.spryng.nl>
* Textmarketer - <https://www.textmarketer.co.uk>
* FreeVoipDeal - <https://www.freevoipdeal.com>
* Nexmo - <https://www.nexmo.com>
* OctoPush - <https://www.octopush.com>
* FreeMobile (FR) - <https://mobile.free.fr>
* Twilio - <https://twilio.com>
* CM Telecom - <https://www.cm.com>
* GatewayAPI - <https://gatewayapi.com>
* SolutionsInfini - <https://solutionsinfini.com>
* Plivo - <https://www.plivo.com>
* Callr - <https://www.callr.com>
* SMSAPI - <https://www.smsapi.com/en>
* OVH SMS PRO - <https://www.ovhtelecom.fr/sms>
* PromoSMS - <https://promosms.com>
* Infobip - <https://www.infobip.com>
* LabsMobile - <https://www.labsmobile.com>
* Tele2 Messaging - <https://portal.tele2messaging.com>

Please note: for these gateways you will need an account with sufficient credits.

* Screenshot(s)
   [phpservmon-ng overview Screenshot](psm-ng.png)
Download
--------

The latest version can be downloaded from https://github.com/TheFoundation/phpservermon-ng/releases.


Requirements
------------

* Web server
* MySQL database
* For PHP5: 5.5.9+
* For PHP7: 7.0.8+
* PHP Extensions (modules)

  * ext-curl
  * ext-ctype
  * ext-filter
  * ext-hash
  * ext-json
  * ext-libxml
  * ext-openssl
  * ext-pdo
  * ext-pcre
  * ext-sockets
  * ext-xml

Install
-------

Please see docs/install.rst.
In a nutshell: unzip, upload, run install.php, enjoy.

If you have downloaded the source from GitHub (and not a pre-built package), the dependencies are not included.
To be able to run an installation from the repo, you need to run the following command to install the dependencies::

     php composer.phar install

If you are familiar with Vagrant (https://www.vagrantup.com)::

     vagrant up

.. and browse to http://localhost:8080/psm/.


Documentation
-------------

The documentation is available in the docs folder or https://docs.phpservermonitor.org.


License
-------

PHP Server Monitor is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

PHP Server Monitor is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with PHP Server Monitor.  If not, see https://www.gnu.org/licenses/.

Docker
-------

PHPServerMonitor ( not NG) is available on Docker : https://github.com/phpservermon/docker-phpservermonitor

