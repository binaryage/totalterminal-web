---
layout: product-home
download: http://downloads.binaryage.com/TotalTerminal-1.5.dmg
downloadtitle: Download v1.5
title: TotalTerminal is a system-wide terminal accessible via a hot-key
product: totalterminal
product_title: TotalTerminal
product_subtitle: a system-wide terminal available on a hot-key
product_icon: /shared/img/icons/totalterminal-256.png
note: If you like TotalTerminal, check out also <a href="http://totalfinder.binaryage.com">TotalFinder</a>.
downloadsubtitle: Requires OS X 10.8 or higher
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
---

<!-- shots: [{
    title: "TotalTerminal's Visor window with nice colors!",
    thumb: "/shared/img/totalterminal-mainshot.png",
    full: "/shared/img/totalterminal-mainshot-full.png"
}] -->

{% contentfor product-buttons %}
<div class="product-buttons">
  <div class="button-container">
    <a href="{{page.download}}" id="o-download-button" class="button product-button-download">
      <span><i class="fa fa-download fa-lg"></i>{{page.downloadtitle}}</span>
    </a>
    <div class="button-note">
      <i class="fa fa-laptop"></i> Compatible with OS X 10.8, 10.9 and 10.10<br>
      <a href="#compatibility">Need version for older OS?</a><br>
      <a href="#changelog">What's new?</a><br>
    </div>
  </div>
</div>
{% endcontentfor %}

## About

### TotalTerminal is a plugin for Terminal.app. 

It provides persistent Visor Window which slides down when you press a hot-key (remember Quake console?).

<img src="/shared/img/totalterminal-mainshot-full.png">

## Installation

### TotalTerminal has an installer

  1. Download latest <a href="{{page.download}}">TotalTerminal.dmg</a> and run the installer.
  2. Configure your keyboard trigger by selecting the `Preferences... -> TotalTerminal` and edit your keyboard hot-key. By default it is `CTRL+~`.

Then you can trigger Visor Window with your hot-key from any application to get an instant terminal session.

### To hide Visor window, you can either:

  * re-trigger with your key-combo
  * optionally, you can click off the TotalTerminal window
  * optionally, you can hit ESC (if enabled in TotalTerminal preferences)

## Changelog

<script src="changelog.js" type="text/javascript" charset="utf-8"></script>

<div class="changelogx">
  <div id="changelog-content" class="changelog"></div>
</div>

<script type="text/coffeescript" charset="utf-8">
  nonce = -> (Math.random() + "").substring(2)
  source = "changelog-beta.txt"
  hashToSelector = (h) -> h.replace /\./g, "\\." # http://stackoverflow.com/a/9930611/84283
  
  $.get "#{source}?x=#{nonce()}", (data) ->
    changelog = parsePlaintextChangelog(data)

    getDownloadLinkForVersion = (version) -> "http://downloads.binaryage.com/TotalTerminal-#{version}.dmg"
    getReleaseDateText = (date) -> "released on " + date
    generateChangelogHTML "#changelog-content", changelog, getDownloadLinkForVersion, getReleaseDateText

    # http://stackoverflow.com/a/13952352/84283
    #if window.location.hash
    #  $(document.body).animate
    #    scrollTop: $(hashToSelector(window.location.hash)).offset().top
    #  , 2000
    
</script>

## Compatibility

#### Does TotalTerminal work on OS X 10.10 (Yosemite)?
> Yes, since 1.5.

#### Does TotalTerminal work on OS X 10.9 (Mavericks)?
> Yes, since 1.4.

#### Does TotalTerminal work on OS X 10.8 (Mountain Lion)?
> Yes, since 1.2.

#### Does TotalTerminal work on OS X 10.7 (Lion)?
> No, last compatible version is 1.4.11.

#### Does TotalTerminal work on OS X 10.6 (Snow Leopard)?
> No, last compatible version is 1.3.

#### Does TotalTerminal work on OS X 10.5 (Leopard)?
> No, last compatible version is 1.0.


## FAQ

#### How do I uninstall TotalTerminal?
> You may use Status Menu Icon and select `Uninstall TotalTerminal`. Alternatively you may [download TotalTerminal DMG](#changelog) again and use `TotalTerminal Uninstaller` which is present there.

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

> Please folow [this thread](https://github.com/binaryage/totalterminal/issues/3) to set special flag from command line. Under Mavericks you cannot easily modify Terminal.app's Info.plist - this would break code signature from Apple.

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

## Special Guest

### Ben Stiglitz about Terminal.app

##### Ben is the author of Terminal.app. Kudos!

<embed src='http://rubyconf2008.confreaks.com/player.swf' height='260' width='640' allowscriptaccess='always' allowfullscreen='true' flashvars='file=http%3A%2F%2Frubyconf2008.confreaks.com%2Fvideos%2Fterminalapp-small.mp4&image=images%2Fterminalapp-preview.jpg&plugins=viral-1'/>

[darwin]: http://github.com/darwin
[torsten]: http://github.com/torsten
[pumpkin]: http://github.com/pumpkin
[blinks]: http://github.com/blinks
[cglee]: http://github.com/cglee
[kleinman]: http://github.com/kleinman
[genki]: http://github.com/genki
[ciaran]: http://github.com/ciaran
[evanphx]: http://github.com/evanphx
[contribute]: http://github.com/binaryage/totalterminal