---
isChild: true
anchor:  mac_setup
---

## Mac Setup {#mac_setup_title}

OS X မှာ PHP ကို prepackaged လုပ်ပြီးသားရှိပါတယ် ဒါပေမယ့်ပုံမှန်အားဖြင့်အဲ့ဒါက နောက်ဆုံး version ထက်နောက်ကျနေပါတယ်။ Mountain Lion မှာ 5.3.10၊ Mavericks မှာ 5.4.17 နဲ့ Yosemite မှာ 5.5.9 ရှိပါတယ်၊ ဒါပေမယ့် PHP 5.6 ထွက်လာတဲ့အခါမှာဒါတွေကမလုံလောက်တော့ပါဘူး။

PHP ကို OS X မှာ install ုပ်ဖို့နည်းမျိူးစုံရှိပါတယ်

### Homebrew ကနေ PHP ကို Install လုပ်ခြင်း

[Homebrew] က OS X အတွက် powerful package manager တစ်ခုဖြစ်ပါတယ်၊ သူက PHP နဲ့ အခြား extensions တွေကို install လုပ်ဖို့ သင့်ကိုကူညီနိုင်ပါတယ်။
[Homebrew PHP] ကတော့ repository တစ်ခုဖြစ်ပါတယ် အဲ့ဒါက Homebrew အတွက် PHP နဲ့ပတ်သတ်တဲ့ "formulae" တွေပါဝင်ပါတယ်၊ နောက်ပြီး အဲ့ဒါကသင့်ကို PHP install လုပ်ခွင့်ပြုပါလိမ့်မယ်။

ဒီနေရာမှာတော့၊ သင် `php53`, `php54`, `php55` ဒါမှမဟုတ် `php56` တွေကို `brew install` command နဲ့ install လုပ်နိုင်ပါတယ်၊ နောက်အဲ့ဒါတွေကိုလည်း သင် modify လုပ်ထားတဲ့ `PATH` variable ပေါ်မူတည်ပြီးတော့လည်းပြောင်းလဲနိုင်ပါတယ်။ 


### Install PHP via Macports

The [MacPorts] Project is an open-source community initiative to design an
easy-to-use system for compiling, installing, and upgrading either
command-line, X11 or Aqua based open-source software on the OS X operating
system.

MacPorts supports pre-compiled binaries, so you don't need to recompile every
dependencies from the source tarball files, it saves your life if you don't
have any package installed on your system.

At this point, you can install `php53`, `php54`, `php55` or `php56` using the `port install` command, for example:

    sudo port install php54
    sudo port install php55

And you can run `select` command to switch your active php:

    sudo port select --set php php55

### PHP ကို phpbrew ကနေတစ်ဆင့် Install လုပ်ခြင်း

[phpbrew] က PHP install လုပ်ဖို့ tool တစ်ခုလည်းဖြစ်တယ် နောက် PHP versions တွေကိုလည်း managing လုပ်ပေးပါတယ်။ ဒါက မတူညီတဲ့ applications/projects နှစ်ခုက မတူညီတဲ့ PHP version နှစ်ခုလိုတယ် နောက် သင်က virtual machines လည်းမသုံးဘူးဆိုရင်ဒါကတကယ့်ကိုအသုံးဝင်မှာဖြစ်ပါတယ်။

### Install PHP via Liip's binary installer
Another popular option is [php-osx.liip.ch] which provides one liner installation methods for versions 5.3 through 5.6.
It doesn't overwrite the php binaries installed by Apple, but installs everything in a separate location (/usr/local/php5).

### Compile from Source

နော်ထက်ရွေးချယ်စရာတစ်ခုကတော့ ကိုယ်တိုင် compile လုပ်တာပါဘဲ[compile it yourself][mac-compile]၊ compile လုပ်မယ်ဆိုရင် [Xcode][xcode-gcc-substitution] ဒါမှမဟုတ် Apple's substitute
["Command Line Tools for XCode"] ကို Apple's Mac Developer Center ကနေ download လုပ်ပြီး install လုပ်ထားရပါမယ်။

### All-in-One Installers

အထက်မှာဖော်ပြခဲ့တဲ့ solution တွေကတော့ PHP အတွက်ဘဲဖြေရှင်းသွားတာတွေဖြစ်ပါတယ်၊Apache, Nginx လို Webserver တွေ SQL server တွေကိုတော့ support ပေးမှာမဟုတ်ပါဘူး။ "All-in-one" ဆိုတာကတော့ [MAMP][mamp-downloads] နောက် [XAMPP][xampp] တို့လိုဟာတွေကိုပြောတာပါ။အဲ့ဒါတွေကမှလိုအပ်တဲ့အခြား software တွေပါတစ်ပါးတည်းပေါင်းထည့်ထားမှာပါ၊ ဒါပေမယ့် setup ကတော့တော်တော်လေးအဆင်ပြေပါလိမ့်မယ်။s


[Homebrew]: http://brew.sh/
[Homebrew PHP]: https://github.com/Homebrew/homebrew-php#installation
[MacPorts]: https://www.macports.org/install.php
[phpbrew]: https://github.com/phpbrew/phpbrew
[php-osx.liip.ch]: http://php-osx.liip.ch/
[mac-compile]: http://php.net/install.macosx.compile
[xcode-gcc-substitution]: https://github.com/kennethreitz/osx-gcc-installer
["Command Line Tools for XCode"]: https://developer.apple.com/downloads
[mamp-downloads]: http://www.mamp.info/en/downloads/
[xampp]: http://www.apachefriends.org/en/xampp.html
[brew-php-switcher]: https://github.com/philcook/brew-php-switcher
