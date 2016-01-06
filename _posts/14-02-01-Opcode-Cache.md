---
isChild: true
anchor:  opcode_cache
---

## Opcode Cache {#opcode_cache_title}

PHP file တစ္ခုကို executed လုပ္တဲ့အခါ ေနာက္ကြယ္မွာ opcodes အျဖစ္သို့ အရင္ compiled လုပ္ျပီးေတာ့မွ အဲ့ဒီ opcodes ေတြကို executed လုပ္ပါတယ္။ PHP file တစ္ခုဟာ ျပုျပင္ ေျပာင္းလဲမွု လုပ္မထားဘူးဆိုရင္ opcodes ဟာ အတူတူပဲျဖစ္ပါတယ္။ အဲ့ဒါဆိုရင္ compilation လုပ္တာက CPU resources ကို ျဖုန္းတီးျခင္း သက္သက္ပဲျဖစ္ပါတယ္။

အခုလိုေနရာမ်ိးမွာ opcode caches က အေရးပါလာပါတယ္။ opcodes ေတြကို memory မွာ သိမ္းထားျပီး လိုအပ္တဲ့ အခါ ျပန္သံုးျခင္းအားျခင္းအားျဖင့္ မလိုအပ္တဲ့ compilation ေတြကို မျဖစ္ေစပါဘူး။ opcode cache ကို အသံုးျပုဖို့ ျပင္ဆင္ခ်ိန္ဟာ မိနစ္ အနည္းငယ္ပဲျကာျပီး သင့္ရဲ့ application ကို သိသိသာသာ ျမန္ဆန္ေစမွာ ျဖစ္တဲ့ အတြက္ မသံုးသင့္ဘူးဆိုတဲ့ အေျကာင္းျပခ်က္ေတာ့ မရွိပါဘူး

PHP 5.5 မွာ [OPcache][opcache-book] လို့ေခါ္တဲ့ built-in opcode cache ပါ၀င္လာပါတယ္။ 5.5 အေရွ့ versions ေတြ အတြက္လည္း ရရွိနိုင္ပါတယ္။

opcode caches အေျကာင္းကို ထပ္မံ ဖတ္ရွုနိုင္ပါတယ္။

* [OPcache][opcache-book] (built-in since PHP 5.5)
* [APC] (PHP 5.4 and earlier)
* [XCache]
* [Zend Optimizer+] (part of Zend Server package)
* [WinCache] (extension for MS Windows Server)
* [list of PHP accelerators on Wikipedia][PHP_accelerators]


[opcache-book]: http://php.net/book.opcache
[APC]: http://php.net/book.apc
[XCache]: http://xcache.lighttpd.net/
[Zend Optimizer+]: http://www.zend.com/en/products/zend_server
[WinCache]: http://www.iis.net/download/wincacheforphp
[PHP_accelerators]: http://en.wikipedia.org/wiki/List_of_PHP_accelerators
