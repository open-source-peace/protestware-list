# List of open-source projects containing protestware

## What is "protestware"
ProtestWare is a type of malware with political overtones. Implements unexpected software behavior. Most often, changes do not affect all users, but a certain group according to such criteria as countries, language, time zone, etc. Manifestations can be in the form of displaying political slogans, deliberate failures in the software itself, or causing harm to other user software.


## About this list

This list is based on [CTO Club List](https://docs.google.com/spreadsheets/d/1H3xPB4PgWeFcHjZ7NOPtrcya_Ua4jUolWm-7z9-jSpQ/htmlview?pru=AAABf7z88MA*ITSp0EBrKinw0LjFWZ9tzQ#gid=2074850979), [GreatBookOfGrudges](https://github.com/ThorgrimGrudgebearer/GreatBookOfGrudges), [toxic-repos](https://github.com/stravnik/toxic-repos) and other sources.


## How to update this list

Please open an issue or create a pull request.


Open source projects with protestware
-------------------------------------

### peacenotwar
ProtestWare NPM-package. [repo](https://github.com/RIAEvangelist/peacenotwar)

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


### yandex-xml-library (PHP)

About project: un-official Yandex-XML PHP library. [repo(removed)](https://github.com/AntonShevchuk/yandex)

A version of the [package](https://packagist.org/packages/anton-shevchuk/yandex-xml-library) with a political slogan has been added to packagist, and the sources have been removed from the GitHub. The result is a broken project build. But there are 9 forks on GitHub.


### AWS Terraform modules
[repo](https://github.com/terraform-aws-modules)

Added anti-Russian slogans and meaningless variables to the code. [One of commits](https://github.com/terraform-aws-modules/terraform-aws-eks/commit/fad350d5bf36a7e39aa3840926b4c9968e9f594c)


### retejs/rete

About project: JavaScript framework for visual programming.

Added "StandWithUkraine" postinstall message. [commit](https://github.com/retejs/rete/commit/d3ff828a41f96e34f04619eb44c688c913ee8def)



### composer 

About project: Package Repository Website for Composer (PHP). [repo](https://github.com/composer/packagist)

Added message "StandWithUkrane". [commit](https://github.com/composer/packagist/commit/86244a3695fcaaac9c5ba4257a4314eae1c6d981)


### PHPUnit

About project: testing framework for PHP. [repo](https://github.com/sebastianbergmann/)

Added message "StandWithUkraine". [commit](https://github.com/sebastianbergmann/phpunit/commit/4634e702b5f05f5e948e531eb8b4fc19be40610c)



### Mistape WordPress plugin

<https://wordpress.org/plugins/mistape/>

Through a vulnerability in the popular Mistape plugin, an attacker gains access to the administrator sections, uploads the UnderConstruction plugin, with which it displays arbitrary information on the main page of the site. Usually this is a widget on the topic of current events in Ukraine. The author of the plugin on February 24 made changes to it. I waited until the update was distributed among users and began to exploit the vulnerability that was included there in a few days.

[changeset](https://plugins.trac.wordpress.org/changeset/2684407/)


Projects, where protestware were removed
----------------------------------------


### Vue CLI

[Issue](https://github.com/vuejs/vue-cli/issues/7054)

Transitive dependency on **node-ipc**.

node-ipc has been [version-locked](https://github.com/vuejs/vue-cli/issues/7051) to a previous release by vue/cli-shared-utils, perhaps one of the more popular downstream consumers of the package.

The (transitive) vulnerability in @vue/cli has been fixed. Please update to the latest versions of @vue/cli, either 4.5.16+ or 5.0.3+


### Awesome Prometheus Alerts	

[repo](https://github.com/samber/awesome-prometheus-alerts)

Determines the user's active language and redirects to the page with slogans. In the following commits, the code was removed. [commit](https://github.com/samber/awesome-prometheus-alerts/commit/6bfcdcca165e57c6fa09a561515c33284caa20c2)


### filestash

Filestash web site. [repo](https://github.com/mickael-kerjean/filestash-website)

Using the definition of IP, Zelensky's video message was shown. [commit](https://github.com/mickael-kerjean/filestash-website/commit/c30a31a583c827182c92cb8ec4b5e8ba1d854c3d)

Now removed.


### tasmota	

About project: ESP8266 / ESP32 firmware. [repo](https://github.com/arendst/Tasmota/)

Messages in the log, inoperability of the device:
[commit](https://github.com/arendst/Tasmota/commit/98cbf2587a1a914bbd16996ebb48dd451d3da448)


The author rolled back the vulnerability under public pressure:
[commit 1](https://github.com/arendst/Tasmota/commit/ba32044bb25b820a104428585bf4c91c4e927f88) |
[commit 2](https://github.com/arendst/Tasmota/commit/b4f99bb74704e4a5f85b7ba9e03b126bf1c43320)


### Onefetch

About project: A command-line Git information tool. [repo](https://github.com/o2sh/onefetch)

When installing the program, it replaces the libgcc_s.so.1 library, the system stops responding and after rebooting the system gives a kernel panic error.

There is no evidence of malice. False alarm.
