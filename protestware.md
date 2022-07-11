# Open source projects with protestware

## peacenotwar

About project: ProtestWare NPM-package. [repo](https://github.com/RIAEvangelist/peacenotwar)

If any users are using IP in Russia or Belarus, all their file will be [wiped entirely by hearts](https://security.snyk.io/vuln/SNYK-JS-PEACENOTWAR-2426724).


## node-ipc

About project: NPM-module for Inter Process Communication. [repo](https://github.com/RIAEvangelist/node-ipc)

[CVE-2022-23812](https://nvd.nist.gov/vuln/detail/CVE-2022-23812)

[Issue](https://github.com/RIAEvangelist/node-ipc/issues/233) |
[Malware code](https://github.com/RIAEvangelist/node-ipc/blob/847047cf7f81ab08352038b2204f0e7633449580/dao/ssl-geospec.js) |
[commit](<https://github.com/RIAEvangelist/node-ipc/commit/1220522453a0388cb4af1a74fe9a0482b6b3a9f3>)

If any users are using IP in Russia or Belarus, all their file will be wiped entirely with a heart emoji.
Manually set a 25% probability at the beginning of the timeout, so that this thing looks more like a floating bug than something intentional.

This affects the package node-ipc from 10.1.1 and before 10.1.3. From versions 11.0.0 onwards, instead of having malicious code directly in the source of this package, node-ipc imports the **peacenotwar** package.

[List of dependent modules](https://github.com/zlw9991/node-ipc-dependencies-list/)


## es5-ext
About project: ECMAScript extensions. [repo](https://github.com/medikoo/es5-ext)

The popular [npm-package](https://www.npmjs.com/package/es5-ext) which has not been updated for 2 years has started receiving regular updates that contain both propaganda and timezone code that increases resource utilization. Check the file `_postinstall.js`

[Issue](https://github.com/medikoo/es5-ext/issues/116) |
[commit](https://github.com/medikoo/es5-ext/commit/28de285ed433b45113f01e4ce7c74e9a356b2af2)


## EventSource

About project: EventSource polyfill. [repo](https://github.com/Yaffle/EventSource)

[Issue](https://github.com/Yaffle/EventSource/issues/199) | [commit](https://github.com/Yaffle/EventSource/commit/de137927e13d8afac153d2485152ccec48948a7a) | [code](https://github.com/Yaffle/EventSource/blob/master/src/eventsource.js#L1032)

The library displays political slogans on your site. To do this, it uses the alert() function with a 15 sec timeout if the user's time zone is Russian. After that, the library opens a political/malicious website in a pop-up window.


## Evolution CMS

01.03.2022 since versions 3.1.10 and 1.4.17 political image added to the admin panel.
[сommit](https://github.com/evolution-cms/evolution/commit/1c586bc76f739264dcf0482530945875fa444b77)

The project was forked as [Evolution CMS Community Edition](https://github.com/evocms-community/evolution) to continue development without any  political slogans.

## voicybot 
About project: bot for Telegram. [repo](https://github.com/backmeupplz/voicy)

02.03.2022 Promo bot message modified to political slogan.
[Issue](https://github.com/backmeupplz/voicy/issues/57) |
[commit](https://github.com/backmeupplz/voicy/commit/1da565a80ab8f2681fddbcf443df60e6a7a15fa5)


## yandex-xml-library (PHP)

About project: un-official Yandex-XML PHP library. [repo(removed)](https://github.com/AntonShevchuk/yandex)

A version of the [package](https://packagist.org/packages/anton-shevchuk/yandex-xml-library) with a political slogan has been added to packagist, and the sources have been removed from the GitHub. The result is a broken project build. But there are 9 forks on GitHub.


## AWS Terraform modules
[repo](https://github.com/terraform-aws-modules)

Added anti-Russian slogans and meaningless variables to the code. [One of commits](https://github.com/terraform-aws-modules/terraform-aws-eks/commit/fad350d5bf36a7e39aa3840926b4c9968e9f594c)


## Mistape WordPress plugin

<https://wordpress.org/plugins/mistape/>

Through a vulnerability in the popular Mistape plugin, an attacker gains access to the administrator sections, uploads the UnderConstruction plugin, with which it displays arbitrary information on the main page of the site. Usually this is a widget on the topic of current events in Ukraine. The author of the plugin on February 24 made changes to it. I waited until the update was distributed among users and began to exploit the vulnerability that was included there in a few days.

[changeset](https://plugins.trac.wordpress.org/changeset/2684407/)


# SweetAlert2

About project: JavaScript popup library. [repo](https://github.com/sweetalert2/sweetalert2)

Added the code to display propaganda and videos. Works only if the user has the Russian language selected in the browser, and the site where the code is executed is located in the .ru/.su/.рф zone. There is [a fork without policy](https://github.com/lofcz/sweetalert2-neutral).

[PR 18.04.2022](https://github.com/sweetalert2/sweetalert2/pull/2428)
[PR 05.07.2022](https://github.com/sweetalert2/sweetalert2/pull/2462)
