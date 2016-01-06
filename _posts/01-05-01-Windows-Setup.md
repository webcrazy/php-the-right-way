---
isChild: true
anchor:  windows_setup
---

## Windows Setup {#windows_setup_title}

Binaries တွေကို [windows.php.net/download][php-downloads] မှာ download လုပ်နိုင်ပါတယ်။ ပြီးရင် PHP ကို extract လုပ်လိုက်ပါ၊ ပြီးရင်ရလာတဲ့ PHP Folder (php,exe ရှိတဲ့ folder) ကို [PATH][windows-path]  မှာ set လုပ်ဖို့ recommended ပေးပါတယ်၊ ဒါမှသင် PHP ကိုမည်သည့်နေရာကမဆိုခေါ်နိုင်မှာဖြစ်ပါတယ်။

လေ့လာဖို့နဲ့ local development အတွက် PHP 5.4 နောက်ပိုင်းပါလာတဲ့ Built in webserver ကိုအသုံးပြုနိုင်ပါတယ်၊ ဒါဆိုသင်အဲ့ဒါတွေ configure လုပ်ဖို့စိုးရိမ်စရာမရှိတော့ဘူးပေါ့။ သင့်အနေနဲ့ webserver နဲ့ MySQL အပြည့်အစုံပါတဲ့ "all in one" တွေကိုအသုံးပြုချင်တယ်ဆိုရင်လည်း [Web Platform Installer][wpi], [XAMPP][xampp], [EasyPHP][easyphp] and [WAMP][wamp] တွေက window development အတွက်ကတော့လွယ်ကူလျင်မြန်ပါလိမ့်မယ်။ ဒါပေမဲ့ အဲ့ဒီ့ tools တွေက production နဲ့ကွာတော့ linux server မှာ deploy လုပ်ရာမှာ environment differences တွေကိုတော့ဂရုပြုရမှဖြစ်ပါတယ်။

တကယ်လို့သင်က production system က Windows ဆိုရင် IIS7 ကအကောင်းဆုံးနဲ့ stable အဖြစ်ဆုံးဖြစ်ပါလိမ့်မယ်။ [phpmanager][phpmanager] (IIS7 အတွက် GUI plugin တစ်ခု) ကိုသုံးပြီးတော့ PHP configuration နဲ့ managing ကို simple ဖြစ်စေပါလိမ့်မယ်။ IIS7 က FastCGI built in ပါတဲ့အတွက်... အသုံးပြုရုံပါဘဲ၊ PHP handler အဖြစ် configure လုပ်ရန်အတွက်ဘဲလိုတာပါ။ support အတွက်နဲ့ additional resources တွေအတွက်ကတော့ [iis.net][php-iis] မှာ PHP အတွက်တွေ့နိုင်ပါတယ်။


[php-downloads]: http://windows.php.net/download/
[windows-path]: http://www.windows-commandline.com/set-path-command-line/
[wpi]: http://www.microsoft.com/web/downloads/platform.aspx
[xampp]: http://www.apachefriends.org/en/xampp.html
[easyphp]: http://www.easyphp.org/
[wamp]: http://www.wampserver.com/en/
[phpmanager]: http://phpmanager.codeplex.com/
[php-iis]: http://php.iis.net/
