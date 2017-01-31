# ioskit.github.io

Which iOS Kit in which iOS version ?... !

## What's New in iOS

- [What's New in iOS](https://developer.apple.com/library/content/releasenotes/General/WhatsNewIniOS/Articles/iOS10.html#//apple_ref/doc/uid/TP40017084-SW1)

### iOS 10

Updates:

- Accelerate, Accounts, AdaptiveLayout, AddressBook, AddressBookUI, AdSupport, ..., AVFoundation, AVKit, AppThinning, AirDrop, AirPlay, AirPrint, ApplePay
- AppThinning, AssetsLibrary, AudioToolbox
- Contacts, ContactsUI

News:

- HapticFeedbacks, Intents, IntentsUI, MessagesApp, ProactiveSuggestions, SiriKit, UserNotifications, UserNotificationsUI

## Setup

* Broken Links checkers
  * http://www.brokenlinkcheck.com/broken-links.php
  * http://www.smartinsights.com/search-engine-optimisation-seo/link-building/site-link-checking-tools/
  * `google3cbd8f0799f83e10.html` is for Google website checker
    * https://www.google.com/webmasters/tools/dashboard?hl=fr&siteUrl=http://ioskit.github.io/&authuser=0

https://github.com/Shopify/liquid/wiki/Liquid-for-Designers
https://docs.shopify.com/themes/liquid-documentation/filters/string-filters#split
http://alanwsmith.com/jekyll-liquid-date-formatting-examples

```
gem install jekyll-gist
```

### Troubleshooting

```
MacBook-Pro-de-Jacques:ioskit.github.io jacques$ jekyll serve --watch
/Users/jacques/.rvm/gems/ruby-2.2.0/gems/safe_yaml-1.0.4/lib/safe_yaml/psych_resolver.rb:4:in `<class:PsychResolver>': uninitialized constant Psych::Nodes (NameError)
	from /Users/jacques/.rvm/gems/ruby-2.2.0/gems/safe_yaml-1.0.4/lib/safe_yaml/psych_resolver.rb:2:in `<module:SafeYAML>'
	from /Users/jacques/.rvm/gems/ruby-2.2.0/gems/safe_yaml-1.0.4/lib/safe_yaml/psych_resolver.rb:1:in `<top (required)>'
	from /Users/jacques/.rvm/rubies/ruby-2.2.0/lib/ruby/2.2.0/rubygems/core_ext/kernel_require.rb:69:in `require'
	from /Users/jacques/.rvm/rubies/ruby-2.2.0/lib/ruby/2.2.0/rubygems/core_ext/kernel_require.rb:69:in `require'
	from /Users/jacques/.rvm/gems/ruby-2.2.0/gems/safe_yaml-1.0.4/lib/safe_yaml/load.rb:131:in `<module:SafeYAML>'
	from /Users/jacques/.rvm/gems/ruby-2.2.0/gems/safe_yaml-1.0.4/lib/safe_yaml/load.rb:26:in `<top (required)>'
	from /Users/jacques/.rvm/rubies/ruby-2.2.0/lib/ruby/2.2.0/rubygems/core_ext/kernel_require.rb:69:in `require'
	from /Users/jacques/.rvm/rubies/ruby-2.2.0/lib/ruby/2.2.0/rubygems/core_ext/kernel_require.rb:69:in `require'
	from /Users/jacques/.rvm/gems/ruby-2.2.0/gems/jekyll-3.3.1/lib/jekyll.rb:29:in `<top (required)>'
	from /Users/jacques/.rvm/rubies/ruby-2.2.0/lib/ruby/2.2.0/rubygems/core_ext/kernel_require.rb:69:in `require'
	from /Users/jacques/.rvm/rubies/ruby-2.2.0/lib/ruby/2.2.0/rubygems/core_ext/kernel_require.rb:69:in `require'
	from /Users/jacques/.rvm/gems/ruby-2.2.0/gems/jekyll-3.3.1/exe/jekyll:6:in `<top (required)>'
	from /Users/jacques/.rvm/gems/ruby-2.2.0/bin/jekyll:23:in `load'
	from /Users/jacques/.rvm/gems/ruby-2.2.0/bin/jekyll:23:in `<main>'
	from /Users/jacques/.rvm/gems/ruby-2.2.0/bin/ruby_executable_hooks:15:in `eval'
	from /Users/jacques/.rvm/gems/ruby-2.2.0/bin/ruby_executable_hooks:15:in `<main>'
```

You can do:

```
gem uninstall psych
gem install psych -v 2.0.5
```

### Versions:

- https://pages.github.com/versions/


## Add new iOS version

* Replace current version in `/_config.xml#currentVersions`
* Update `_kits/*.md#status` and `_features/*.md#status`