# List of open-source projects containing protestware

## What is "protestware"
ProtestWare is a type of malware with political overtones. Implements unexpected software behavior. Most often, changes do not affect all users, but a certain group according to such criteria as countries, language, time zone, etc. Manifestations can be in the form of displaying political slogans, deliberate failures in the software itself, or causing harm to other user software.


## About this list

This list is based on [CTO Club List](https://docs.google.com/spreadsheets/d/1H3xPB4PgWeFcHjZ7NOPtrcya_Ua4jUolWm-7z9-jSpQ/htmlview?pru=AAABf7z88MA*ITSp0EBrKinw0LjFWZ9tzQ#gid=2074850979), its copy on GitHub [toxic-repos](https://github.com/stravnik/toxic-repos) and other sources. 

Note. The list contains only those projects that affect end users or harm developers. The appearance of slogans in the documentation or in the source code is not a reason for inclusion in this list. The list does not include obscure repositories that have less than 10 stars.

If you think that following repos violates GitHub's [Terms of Service](https://github.com/site/terms), you can [report abuse](https://support.github.com/contact/report-abuse?category=report-content&report=other).

## How to update this list

Please open an issue or create a pull request.


Open source projects with protestware
-------------------------------------

### peacenotwar

About project: ProtestWare NPM-package. [repo](https://github.com/RIAEvangelist/peacenotwar)

If any users are using IP in Russia or Belarus, all their file will be [wiped entirely by hearts](https://security.snyk.io/vuln/SNYK-JS-PEACENOTWAR-2426724).


### node-ipc

About project: NPM-module for Inter Process Communication. [repo](https://github.com/RIAEvangelist/node-ipc)

[CVE-2022-23812](https://nvd.nist.gov/vuln/detail/CVE-2022-23812)

[Issue](https://github.com/RIAEvangelist/node-ipc/issues/233) |
[Malware code](https://github.com/RIAEvangelist/node-ipc/blob/847047cf7f81ab08352038b2204f0e7633449580/dao/ssl-geospec.js) |
[commit](<https://github.com/RIAEvangelist/node-ipc/commit/1220522453a0388cb4af1a74fe9a0482b6b3a9f3>)

If any users are using IP in Russia or Belarus, all their file will be wiped entirely with a heart emoji.
Manually set a 25% probability at the beginning of the timeout, so that this thing looks more like a floating bug than something intentional.

This affects the package node-ipc from 10.1.1 and before 10.1.3. From versions 11.0.0 onwards, instead of having malicious code directly in the source of this package, node-ipc imports the **peacenotwar** package.

[List of dependent modules](https://github.com/zlw9991/node-ipc-dependencies-list/)


### es5-ext
About project: ECMAScript extensions. [repo](https://github.com/medikoo/es5-ext)

The popular [npm-package](https://www.npmjs.com/package/es5-ext) which has not been updated for 2 years has started receiving regular updates that contain both propaganda and timezone code that increases resource utilization. Check the file `_postinstall.js`

[Issue](https://github.com/medikoo/es5-ext/issues/116) |
[commit](https://github.com/medikoo/es5-ext/commit/28de285ed433b45113f01e4ce7c74e9a356b2af2)


### EventSource

About project: EventSource polyfill. [repo](https://github.com/Yaffle/EventSource)

[Issue](https://github.com/Yaffle/EventSource/issues/199) | [commit](https://github.com/Yaffle/EventSource/commit/de137927e13d8afac153d2485152ccec48948a7a) | [code](https://github.com/Yaffle/EventSource/blob/master/src/eventsource.js#L1032)

The library displays political slogans on your site. To do this, it uses the alert() function with a 15 sec timeout if the user's time zone is Russian. After that, the library opens a political/malicious website in a pop-up window.


### Evolution CMS

01.03.2022 since versions 3.1.10 and 1.4.17 political image added to the admin panel.
[сommit](https://github.com/evolution-cms/evolution/commit/1c586bc76f739264dcf0482530945875fa444b77)

The project was forked as [Evolution CMS Community Edition](https://github.com/evocms-community/evolution) to continue development without any  political slogans.

### voicybot 
About project: bot for Telegram. [repo](https://github.com/backmeupplz/voicy)

02.03.2022 Promo bot message modified to political slogan. 
[Issue](https://github.com/backmeupplz/voicy/issues/57) |
[commit](https://github.com/backmeupplz/voicy/commit/1da565a80ab8f2681fddbcf443df60e6a7a15fa5)


### yandex-xml-library (PHP)

About project: un-official Yandex-XML PHP library. [repo(removed)](https://github.com/AntonShevchuk/yandex)

A version of the [package](https://packagist.org/packages/anton-shevchuk/yandex-xml-library) with a political slogan has been added to packagist, and the sources have been removed from the GitHub. The result is a broken project build. But there are 9 forks on GitHub.


### AWS Terraform modules
[repo](https://github.com/terraform-aws-modules)

Added anti-Russian slogans and meaningless variables to the code. [One of commits](https://github.com/terraform-aws-modules/terraform-aws-eks/commit/fad350d5bf36a7e39aa3840926b4c9968e9f594c)


### Mistape WordPress plugin

<https://wordpress.org/plugins/mistape/>

Through a vulnerability in the popular Mistape plugin, an attacker gains access to the administrator sections, uploads the UnderConstruction plugin, with which it displays arbitrary information on the main page of the site. Usually this is a widget on the topic of current events in Ukraine. The author of the plugin on February 24 made changes to it. I waited until the update was distributed among users and began to exploit the vulnerability that was included there in a few days.

[changeset](https://plugins.trac.wordpress.org/changeset/2684407/)


Projects that cancel Russia
---------------------------

List of projects that demonstrate [cancel culture](https://en.wikipedia.org/wiki/Cancel_culture) towards Russia.

### Quake3e

About project: Improved Quake III Arena engine. [repo](https://github.com/ec-/Quake3e)

26.02.2022 Removed support of Russian MCST/Elbrus platform: [commit](https://github.com/ec-/Quake3e/commit/50167f34e361bac156315e53efccb5a5d4acac80)


### RESP.app / RedisDesktopManager
GUI for Redis. [repo](https://github.com/uglide/RedisDesktopManager/)

Russian translation was removed. [commit](https://github.com/uglide/RedisDesktopManager/commit/8b2b357d9d233100f84a69f81ed22b8caa04fa22)


### pnpm

About project: Package manager. [repo](https://github.com/pnpm/pnpm/)

Added anti-Russian statement. [commit](https://github.com/pnpm/pnpm/commit/3c328ec465c597ff558c1f38afbfe2a0c1b02a83)

Also access to pnpm.io is blocked from Russia an Belarus


### Qalculate!

About project: cross-platform desktop calculator. [repo](https://github.com/Qalculate/qalculate-gtk)

14.03.2022 Russian and Belarus flags were removed for national currencies.

[Issue](https://github.com/Qalculate/qalculate-gtk/issues/389) | [commit](https://github.com/Qalculate/qalculate-gtk/commit/74c7413429b386f08028565f16f537204217b456)

### Yet Another Dialog

About project: program allows you to display GTK+ dialog boxes from command line. [repo](https://github.com/v1cont/yad)

02.03.2022 Russian locale removed. [commit](https://github.com/v1cont/yad/commit/e38f7fa71aa9b2dff408ae14ca7133e4fdc4b02a)


Projects, where protestware were removed
----------------------------------------

### Awesome Prometheus Alerts	

[repo](https://github.com/samber/awesome-prometheus-alerts)

Determines the user's active language and redirects to the page with slogans. In the following commits, the code was removed. [commit](https://github.com/samber/awesome-prometheus-alerts/commit/6bfcdcca165e57c6fa09a561515c33284caa20c2)


### tasmota	

About project: ESP8266 / ESP32 firmware. [repo](https://github.com/arendst/Tasmota/)

Messages in the log, inoperability of the device:
[commit](https://github.com/arendst/Tasmota/commit/98cbf2587a1a914bbd16996ebb48dd451d3da448)


The author rolled back the vulnerability under public pressure:
[commit 1](https://github.com/arendst/Tasmota/commit/ba32044bb25b820a104428585bf4c91c4e927f88) |
[commit 2](https://github.com/arendst/Tasmota/commit/b4f99bb74704e4a5f85b7ba9e03b126bf1c43320)

