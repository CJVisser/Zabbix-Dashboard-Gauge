![Dashboard Gauge](images/gauge-image-small.png)
# Zabbix-Dashboard-Gauge
Add a Gauge Widget to your Zabbix Dashboards.

## What's new
##### March 13, 2022
* Initial Public Beta Release

## About the Gauge
The design of the Zabbix Gauge Widget is borrowed heavily from [Google Chart's 'Gauge'](https://developers.google.com/chart/interactive/docs/gallery/gauge). It tries to support all of the features of the google release, but it is renders as svg in zabbix using native function calls, so no external javascript or additional libraries are required.

Configuration of the gauge supports naming the widget, labeling the gauge, selecting your item, the gauge range, displaying the number of 'minor ticks' between 'major ticks', and highlighting up to 3 regions of the gauge to indicate normal and problem value ranges.  The gauge also shows the value with units currently displayed.

## What's inside
The installer script and related patch add functionality to zabbix-web to display item values in a gauge-style widget. _gauge-installer_ is an interactive script, it will confirm your zabbix docroot, zabbix release, backup your docroot into a tar file, and attempt a dry-run of the install before asking you if you really really want to install it.  There is also an option to reverse the install.  See the section "Working with Patches" for more info. 

## Prerequisites
* Zabbix 6.0.1
* Linux binaries: patch, date, grep, cut, date, bash

## Install
1. Download gauge-installer and the patch file for your Zabbix release
2. As root, run _gauge-installer_, follow the prompts, and complete a successful install
3. Restart your web server  

## Working with Patches
Working with patches is a bit different from rpms, and you definitely can break stuff badly if you're not careful.  The gauge-installer script tries to keep you from doing 'bad things' and it will backup your docroot to a tar file before install.  You should remember to always reverse the patch before upgrading zabbix-web.

## Configuring the widget
TBD

## Bugs
There are quite a few.  Head over to [issues](issues/) to see them all.  Please report any new ones.
