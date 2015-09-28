---
layout: product-home
download: http://downloads.binaryage.com/TotalTerminal-1.6.dmg
downloadtitle: Download v1.6
title: TotalTerminal is a system-wide terminal accessible via a hot-key
product: totalterminal
product_title: TotalTerminal
product_subtitle: a system-wide terminal available on a hot-key
product_icon: /shared/img/icons/totalterminal-256.png
fbsdk: 1
plusone: 1
product-fblike: 1
product-plusone: 1
product-tweet: 1
repo: http://github.com/binaryage/totalterminal
meta_title: TotalTerminal is a system-wide terminal accessible via a hot-key
meta_keywords: totalterminal,terminal,osx,simbl,binaryage,productivity,software,visor
meta_description: TotalTerminal is a plugin for Terminal.app which provides Quake-style terminal window available on keyboard shortcut
meta_image: /shared/img/icons/totalterminal-128.png
build_tabs: 1
ogmeta: {
    site_name: "BinaryAge website",
    description: "TotalTerminal is a system-wide terminal for OS X available on a hot-key",
    email: "support@binaryage.com",
    type: "product",
    title: "TotalTerminal",
    url: "http://totalterminal.binaryage.com",
    image: "http://www.binaryage.com/shared/img/icons/totalterminal-256.png"
}
oses: [{
  version: "10.11",
  label: "El Capitan",
  logo: "logo-el-capitan.png",
  wiki: "OS_X_El_Capitan",
  note: "install <a href=\"#latest\">the latest version</a>, but <a href=\"/#sip\" class=\"red\">needs a system tweak</a>"
},{
  version: "10.10",
  label: "Yosemite",
  logo: "logo-yosemite.png",
  wiki: "OS_X_Yosemite",
  note: "install <a href=\"#latest\">the latest version</a>"
},{
  version: "10.9",
  label: "Mavericks",
  logo: "logo-mavericks.png",
  wiki: "OS_X_Mavericks",
  note: "install <a href=\"#latest\">the latest version</a>"
},{
  version: "10.8",
  label: "Mountain Lion",
  logo: "logo-mountain-lion.png",
  wiki: "OS_X_Mountain_Lion",
  note: "install <a href=\"#1.5.4\">version 1.5.4</a>"
},{
  version: "10.7",
  label: "Lion",
  logo: "logo-lion.png",
  wiki: "OS_X_Lion",
  note: "install <a href=\"#1.4.11\">version 1.4.11</a>"
},{
  version: "10.6",
  label: "Snow Leopard",
  logo: "logo-snow-leopard.png",
  wiki: "OS_X_Snow_Leopard",
  note: "install <a href=\"#1.3\">version 1.3</a>"
}]
---

{% contentfor product-buttons %}
<div class="product-buttons">
  <div class="button-container">
    <div class="cross-promo">
      <i class="fa fa-thumbs-o-up fa-lg"></i><div>Do you like TotalTerminal?<br><a href="http://totalfinder.binaryage.com">Check out also TotalFinder</a></div>.
    </div>
  </div>
  <div class="button-container">
    <a href="{{page.download}}" id="o-download-button" class="button product-button-download">
      <span><i class="fa fa-download fa-lg"></i>{{page.downloadtitle}}</span>
    </a>
    <div class="button-note">
      <i class="fa fa-check-circle"></i> Compatible with OS X 10.8, 10.9 and 10.10<br>
      <div class="exclamation"><i class="fa fa-exclamation-circle"></i> <a href="/#sip">Not compatible with OS X 10.11</a></div><br>
      <br>
      <a href="#compatibility">Looking for an older version?</a><br>
      <a href="#changelog">What's new?</a><br>
    </div>
  </div>
</div>
{% endcontentfor %}

## About

<div class="license-desk exclamation" style="display:inline-block">
Warning: TotalTerminal is no longer under active development
</div>

### TotalTerminal is a plugin for Terminal.app. 

It provides persistent Visor Window which slides down when you press a hot-key (remember Quake console?).

<img src="/shared/img/totalterminal-mainshot-full.png" class="doc-main-image">

## Installation

### TotalTerminal has an installer

  1. Download <a href="{{page.download}}">latest TotalTerminal.dmg</a> and run the installer.
  2. Configure your keyboard trigger by selecting the `Preferences... -> TotalTerminal` and edit your keyboard hot-key. By default it is `CTRL+~`.

Then you can trigger Visor Window with your hot-key from any application to get an instant terminal session.

### To hide Visor window, you can either:

  * re-trigger with your key-combo
  * optionally, you can click off the TotalTerminal window
  * optionally, you can hit ESC (if enabled in TotalTerminal preferences)

## Compatibility

{% contentfor inline_styles %}
.custom-os-box { margin-left:20px; font-size:14px; clear:both; margin-bottom:20px; line-height:32px; }
.custom-os-box img { height:32px; float:left; margin-right:12px; }
.custom-os-box .title { color:#666; font-weight:bold; display:inline-block; width: 220px }
.custom-os-box .title a { color:#666; }
.custom-os-box .note { color:#666; display:inline-block }
.custom-os-box a {font-weight: bold}
{% endcontentfor %}

{% for item in page.oses %}
<div class="custom-os-box">
  <img src="shared/img/os/{{item.logo}}">
  <div class="title"><a href="http://en.wikipedia.org/wiki/{{item.wiki}}">OS X {{item.version}} ({{item.label}})</a></div><div class="note"> =&gt; {{item.note}}</div>
</div>
{% endfor %}

For older versions please search the internet for <a href="http://www.blacktree.com">Visor by Blacktree</a>.

## FAQ

#### Does it run under OS X 10.11 (El Capitan)?
>  Not under default configuration. It requires a system tweak, [read about it here](/#sip).

#### How do I uninstall TotalTerminal?
> You may use Status Menu Icon and select `Uninstall TotalTerminal`. Alternatively you may [download TotalTerminal DMG](#changelog) again and use `TotalTerminal Uninstaller` which is present there.
>
> Alternatively you can launch this command in Terminal.app:
> `open "/Library/ScriptingAdditions/TotalTerminal.osax/Contents/Resources/TotalTerminal.bundle/Contents/Resources/TotalTerminal Uninstaller.app"`


#### What is the difference between Visor.bundle and TotalTerminal.app?
> TotalTerminal supersedes Visor. Visor.bundle is a SIMBL plugin which was originally written by Nicholas Jitkoff from [Blacktree](http://blacktree.com). Original Visor was introduced for OS X - Tiger. I have been developing it since Leopard. I decided to rename it to TotalTerminal with OS X Lion release. TotalTerminal has installer, Sparkle updater and does not depend on [SIMBL](http://www.culater.net/software/SIMBL/SIMBL.php). In the future it will get more bug fixes and hopefully some new features.
>
> The main technical difference is that TotalTerminal is not launched automatically. You have to launch TotalTerminal.app to inject plugin into Terminal.app (if it is not running the launcher will launch it)

#### I see two Terminal.app icons in the Dock. How should I get rid of it?

> This affects people who pin TotalTerminal.app icon in the Dock as a permanent icon.
>
>When you click TotalTerminal.app icon in the Dock, the system launches TotalTerminal.app. But [TotalTerminal.app is just a lightweight launcher](https://github.com/binaryage/totalterminal-installer/tree/master/TotalTerminal.app) which:
>
>  1. launches Terminal.app (if it is not running)
>  2. injects TotalTerminal plugin into it.
>  3. quits
>
>You end up with two Terminal icons in the Dock: one for running Terminal.app and second for pinned TotalTerminal.app (which is not running anymore after injecting the plugin).
>

#### How to remove Terminal from App Switcher (CMD+TAB)?

> Please follow [this thread](https://github.com/binaryage/totalterminal/issues/3) to set special flag from command line. Under Mavericks you cannot easily modify Terminal.app's Info.plist - this would break code signature from Apple.

#### Where are TotalTerminal settings stored?
> TotalTerminal settings are stored with Terminal.app settings. You can `open ~/Library/Preferences/com.apple.Terminal.plist` and tweak the values (better to do this when Terminal.app is not running).
If you have troubles with TotalTerminal settings, delete this file and restart Terminal.app. The file will be recreated with default values.

#### How can I open a new terminal window the old way, as a classic OSX window?
> If there is a Visor Window (the status menu icon is active) every new terminal window will be opened as a classic OS X window. In other words, open at least two terminal windows. The second one will be a classic terminal window for sure.

#### How can I change the height of Visor?
> Go to Terminal.app's Preferences -> Window -> Rows

#### How can I stick Visor to left screen edge?
> Look for the "Position" option in TotalTerminal Preferences and pick "Left-Stretch" window placement.

#### How can I change the width of Visor?
> By default Visor Window stretches to the full screen width. Set some non-stretching positioning for Visor Window in TotalTerminal Preferences, then Go to Terminal.app's Preferences -> Window -> Columns.

#### Is it possible to show Visor only on a secondary monitor?
> Go to TotalTerminal Preferences -> Screen

#### Is it possible to see Visor on every Space?
> TotalTerminal forces Visor window to be visible on every space. You may disable this in TotalTerminal Preferences. Note: Spaces configuration for Terminal.app doesn't apply to the Visor Window, it is effective only for other (classic) terminal windows.

#### I want to keep different preferences for Visor and other (classic) terminal windows. What is the best way manage this?
> There may be a profile in Terminal.app called "Visor". Visor Window attempts to use the "Visor" profile when opening new tabs in Visor Window (regardless of "default profile" or "startup profile" settings in Terminal.app). In case "Visor" profile is not present, it uses currently selected default profile.

#### Do I need to install TerminalColours SIMBL with TotalTerminal?
> No, TerminalColours is integrated into TotalTerminal 1.0 and later. Actually it conflicts with TotalTerminal if installed as SIMBL plugin.

#### Do I need to install CopyOnSelect SIMBL with TotalTerminal?
> No, CopyOnSelect is integrated into TotalTerminal 1.0 and later. It is a configurable option in TotalTerminal Preferences (disabled by default).

## SIP

### System Integrity Protection

Under OS X 10.11 (El Capitan), TotalTerminal cannot run on a normally configured machine due to [System Integrity Protection](https://en.wikipedia.org/wiki/System_Integrity_Protection).

System Integrity Protection (SIP) is a new security feature introduced by Apple. That's good, but unfortunately it prevents TotalTerminal from augmenting Finder. This article will tell you how to configure your machine, so that you can use TotalTerminal. Before you do this, it is important to get informed about [what System Integrity Protection is, and what it means to turn it off](https://en.wikipedia.org/wiki/System_Integrity_Protection). Apple also provided [some information here](https://developer.apple.com/library/prerelease/mac/documentation/Security/Conceptual/System_Integrity_Protection_Guide/Introduction/Introduction.html).

<div class="license-desk">
<a href="http://binaryage.com/about">
<img width="20" height="20" src="http://www.gravatar.com/avatar/79322c2ed80c2d722de8c9d0475198a0?s=40" style="float: left; position: relative; top: 2px; margin-right: 6px; display:block; border: 1px solid #ccc" title="Who is Antonin?">
</a>
Do you really depend on TotalTerminal workflows so much that you want to possibly lower your system security?
Frankly, I'm going to stop TotalTerminal development because I have personally switched to <a href="https://iterm2.com/">iTerm 2</a>. It offers similar functionality to Visor and comparable features to build-in Terminal.app.
</div>

Anyways, if you decide to modify the setting under El Capitan, you will be able to install and run TotalTerminal as before. Just to be clear...

<div class="license-desk exclamation">
I'm not encouraging you to turn System Integrity Protection off. Your machine may be less secure with it off. It is entirely your decision.
</div>

<br>

### How to modify System Integrity Protection

You must boot into the Recovery OS. You do this by restarting your machine, and holding `COMMAND + R` until the Apple logo appears.

Then select Terminal from the Utilities menu. It looks like this:

<img src="/images/recovery-1.png">

In the window that opens, type `csrutil enable --without debug` and press return. 

<img src="/images/recovery-2.png">

This turns off the part of SIP that TotalTerminal needs to run, and OS X complains that it is an unsupported configuration.

Now type `reboot` and press return to restart your machine. After restart you may install the [latest version of TotalTerminal](/#changelog).

You can find some further information [in our blog](http://blog.binaryage.com/el-capitan-update).

## Changelog

<script src="shared/js/changelog.js" type="text/javascript" charset="utf-8"></script>

<div class="changelogx">
  <div id="changelog-content" class="changelog"></div>
</div>

<script type="text/coffeescript" charset="utf-8">
  nonce = -> (Math.random() + "").substring(2)
  source = "changelog-beta.txt"
  
  $.get "#{source}?x=#{nonce()}", (data) ->
    changelog = parsePlaintextChangelog(data)

    getDownloadLinkForVersion = (version) -> "http://downloads.binaryage.com/TotalTerminal-#{version}.dmg"
    getReleaseDateText = (date) -> "released on " + date
    generateChangelogHTML "#changelog-content", changelog, getDownloadLinkForVersion, getReleaseDateText
    $(window).trigger "changelog-rendered"
    
</script>

