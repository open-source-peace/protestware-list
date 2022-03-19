# List of open-source projects containing protestware

## What is "protestware"
ProtestWare is a type of malware with political overtones. Implements unexpected software behavior. Most often, changes do not affect all users, but a certain group according to such criteria as countries, language, time zone, etc. Manifestations can be in the form of displaying political slogans, deliberate failures in the software itself, or causing harm to other user software.


## About this list

This list is based on [CTO Club List](https://docs.google.com/spreadsheets/d/1H3xPB4PgWeFcHjZ7NOPtrcya_Ua4jUolWm-7z9-jSpQ/htmlview?pru=AAABf7z88MA*ITSp0EBrKinw0LjFWZ9tzQ#gid=2074850979) and other sources.


## How to update this list

Please open an issue or create a pull request.


Open source projects with protestware
-------------------------------------


### peacenotwar
<https://github.com/RIAEvangelist/peacenotwar>

If any users are using IP in Russia or Belarus, all their file will be [wiped entirely by hearts](https://security.snyk.io/vuln/SNYK-JS-PEACENOTWAR-2426724).

### node-ipc

<https://nvd.nist.gov/vuln/detail/CVE-2022-23812>

<https://github.com/RIAEvangelist/node-ipc/issues/233>
<https://github.com/RIAEvangelist/node-ipc/blob/847047cf7f81ab08352038b2204f0e7633449580/dao/ssl-geospec.js>
<https://github.com/RIAEvangelist/node-ipc/commit/1220522453a0388cb4af1a74fe9a0482b6b3a9f3>

If any users are using IP in Russia or Belarus, all their file will be wiped entirely with a heart emoji.
Manually set a 25% probability at the beginning of the timeout, so that this thing looks more like a floating bug than something intentional.

This affects the package node-ipc from 10.1.1 and before 10.1.3. From versions 11.0.0 onwards, instead of having malicious code directly in the source of this package, node-ipc imports the **peacenotwar** package
[List of dependent modules](https://github.com/zlw9991/node-ipc-dependencies-list/)

### es5-ext
The popular library <https://www.npmjs.com/package/es5-ext>  which has not been updated for 2 years has started receiving regular updates that contain both propaganda and timezone code that increases resource utilization. Check this file - `_postinstall.js`

<https://github.com/medikoo/es5-ext/issues/116>
<https://github.com/medikoo/es5-ext/commit/28de285ed433b45113f01e4ce7c74e9a356b2af2>

Has anti-war manifest.


### RedisDesktopManager

<https://github.com/uglide/RedisDesktopManager/commit/8b2b357d9d233100f84a69f81ed22b8caa04fa22>

Russian language was removed.

### pnpm

<https://github.com/pnpm/pnpm/commit/3c328ec465c597ff558c1f38afbfe2a0c1b02a83>
<https://github.com/pnpm/pnpm/commit/0066c11b9779971349d323c9fffced0271535cb7>

Block access to pnpm.io from Russia an Belarus

### yandex-xml-library

Un-Official Yandex-XML PHP library <https://packagist.org/packages/anton-shevchuk/yandex-xml-library>

A version of the package with a political slogan has been added to packagist, and the sources have been removed from the github. The result is a broken project build.


### AWS Terraform modules
<https://github.com/terraform-aws-modules>

added anti-Russian slogans and meaningless variables to the code:
<https://github.com/terraform-aws-modules/terraform-aws-eks/commit/fad350d5bf36a7e39aa3840926b4c9968e9f594c>


### retejs/rete

<https://github.com/retejs/rete/commit/d3ff828a41f96e34f04619eb44c688c913ee8def>

"StandWithUkraine" postinstall message


### composer 

Package Repository Website for Composer (PHP)	

<https://github.com/composer/packagist/commit/86244a3695fcaaac9c5ba4257a4314eae1c6d981>

Message "StandWithUkrane"


### PHPUnit
<https://github.com/sebastianbergmann/phpunit/commit/4634e702b5f05f5e948e531eb8b4fc19be40610c>

Message "StandWithUkraine"


### Mistape WordPress plugin

<https://wordpress.org/plugins/mistape/>

Through a vulnerability in the popular Mistape plugin, an attacker gains access to the administrator sections, uploads the UnderConstruction plugin, with which it displays arbitrary information on the main page of the site. Usually this is a widget on the topic of current events in Ukraine. The author of the plugin on February 24 made changes to it. I waited until the update was distributed among users and began to exploit the vulnerability that was included there in a few days.
<https://plugins.trac.wordpress.org/changeset/2684407/>


Projects, where protestware were removed
----------------------------------------


### Vue CLI

<https://github.com/vuejs/vue-cli/issues/7054>

Transitive dependency on **node-ipc**.

node-ipc has been [version-locked](https://github.com/vuejs/vue-cli/issues/7051) to a previous release by vue/cli-shared-utils, perhaps one of the more popular downstream consumers of the package.

The (transitive) vulnerability in @vue/cli has been fixed. Please update to the latest versions of @vue/cli, either 4.5.16+ or 5.0.3+


### Awesome Prometheus Alerts	
<https://github.com/samber/awesome-prometheus-alerts/commit/6bfcdcca165e57c6fa09a561515c33284caa20c2>

Determines the user's active language and redirects to the page with slogans. In the following commits, the code was removed.


### filestash
https://github.com/mickael-kerjean/filestash-website/commit/c30a31a583c827182c92cb8ec4b5e8ba1d854c3d

Using the definition of IP, Zelensky's video message was shown. Now removed


### tasmota	
ESP8266 / ESP32 firmware.

Messages in the log, inoperability of the device:
<https://github.com/arendst/Tasmota/commit/98cbf2587a1a914bbd16996ebb48dd451d3da448>


The author rolled back the vulnerability under public pressure:
<https://github.com/arendst/Tasmota/commit/ba32044bb25b820a104428585bf4c91c4e927f88>
<https://github.com/arendst/Tasmota/commit/b4f99bb74704e4a5f85b7ba9e03b126bf1c43320>


### Onefetch

<https://github.com/o2sh/onefetch>

When installing the program, it replaces the libgcc_s.so.1 library, the system stops responding and after rebooting the system gives a kernel panic error.

There is no evidence of malice. False alarm.
