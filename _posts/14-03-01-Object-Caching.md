---
isChild: true
anchor:  object_caching
---

## Object Caching {#object_caching_title}

There are times when it can be beneficial to cache individual objects in your code, such as with data that is expensive to get or database calls where the result is unlikely to change. You can use object caching software to hold these pieces of data in memory for extremely fast access later on. If you save these items to a data store after you retrieve them, then pull them directly from the cache for following requests, you can gain a significant improvement in performance as well as reduce the load on your database servers.

သင့္ရဲ့ code ထဲမွာ တစ္ခ်ို့ေသာ object  ေတြ ဥပမာ ... ရဖို့ခက္ခဲတဲ့ data ေတြ၊ ေျပာင္းလဲနိုင္ေျခ နည္းတဲ့ database calls ေတြကို  cache လုပ္မယ္ဆိုရင္ အက်ိုးရွိပါတယ္။ ေနာက္တစ္ခါသံုးဖို့ လိုအပ္တဲ့ အခါ အရမ္းျမန္ဆန္ေအာင္ memory မွာ အဲ့ဒီ data ေတြကို သိမ္းထားဖို့ object caching software  ကို အသံုးျပုနိုင္ပါတယ္။ အဲ့ဒီ item  ေတြကို ပထမတစ္ျကိမ္ရယူျပီးရင္ data store ထဲ ထည့္ထား၊ ေနာက္ထပ္ ဒါမ်ိုး request ေတြဆိုရင္ cache ထဲက ေနတိုက္ရိုက္ယူဆိုျပီး ျပုလုပ္ထားမယ္ဆိုရင္ performance အရေ ျမန္ဆန္ျခင္းေရာ database server ကို load လုပ္ ျခင္းကို လည္း ေလ်ာ့ခ်နိုင္မွာပါ။

Many of the popular bytecode caching solutions let you cache custom data as well, so there's even more reason to take
advantage of them. APCu, XCache, and WinCache all provide APIs to save data from your PHP code to their memory cache.

နာမည္ျကီး bytecode caching solutions ေတြဟာ custom data ေတြကို ပါ cache လုပ္နိုင္ျပီး သူတို့ေတြကေန ရနိုင္တဲ့ တျခား အက်ိုးေက်းဇူး အမ်ားအျပားလည္းရွိပါေသးတယ္။  APCu, XCache, နဲ့ WinCache တို့ အကုန္လံုးဟာ သင့္ရဲ့ PHP code ေတြကို သူတို့ရဲ့ memory cache ေတြမွာ save ဖို့အတြက္ APIs ေတြေပးထားပါတယ္။

The most commonly used memory object caching systems are APCu and memcached. APCu is an excellent choice for object
caching, it includes a simple API for adding your own data to its memory cache and is very easy to setup and use. The
one real limitation of APCu is that it is tied to the server it's installed on. Memcached on the other hand is
installed as a separate service and can be accessed across the network, meaning that you can store objects in a
hyper-fast data store in a central location and many different systems can pull from it.

လူသံုးအမ်ားဆံုး memory object caching systems ေတြကေတာ့ APCu and memcached တို့ပဲျဖစ္ပါတယ္။ APCu က object caching အတြက္ အေကာင္းဆံုး ေရြးခ်ယ္မွုျဖစ္ျပီး သင့္ရဲ့ data ေတြကို သူ့ရဲ့ memory cache ထဲထည့္ဖို့ setup လုပ္ရန္လြယ္ကူျပီး ရိုးရွင္တဲ့ API ပါဝင္ပါတယ္။ APCu ရဲ့ တစ္ခုတည္းေသာ ကန့္သတ္ခ်က္က သူ့ကို installed  လုပ္ထားတဲ့ server နဲ့ တြဲေနျခင္းပဲ ျဖစ္ပါတယ္။ Memcached ကေတာ့ သီးသန့္ service အျဖစ္ installed လုပ္ သံုးနိုင္ျပီး network မွ တစ္ဆင့္ access လုပ္နိုင္ပါတယ္။ ဆိုလိုတာက object ေတြကို အရမ္းျမန္ဆန္တဲ့ ေနရာတစ္ခုမွာ သိမ္းထားျပီး system အမ်ိုးမ်ိုးကေန ရယူအသံုးျပုနုိင္ပါတယ္။

Note that when running PHP as a (Fast-)CGI application inside your webserver, every PHP process will have its own cache,
i.e. APCu data is not shared between your worker processes. In these cases, you might want to consider using memcached
instead, as it's not tied to the PHP processes.

တစ္ခု သတိထားရမွာက PHP ကို သင့္ ရဲ့ webserver မွာ (Fast-)CGI application အျဖစ္ run ထားမယ္ဆိုရင္ေတာ့ PHP process တစ္ခုစီမွာ သူ့ကိုယ္ပိုင္ cache ရွိျပီးသားပါ။ ဥပမာ။ ။APCu data ေတြဟာ worker process တစ္ခုနဲ့ တစ္ခု ျကား share မလုပ္ပါဘူး။ အဲ့ဒါမ်ိုးဆိုရင္ေတာ့ PHP process ေတြနဲ့ တြဲစပ္မထားတဲ့ memcached ကို သံုးဖို့ စဥ္းစားသင့္ပါတယ္။

In a networked configuration APCu will usually outperform memcached in terms of access speed, but memcached will be
able to scale up faster and further. If you do not expect to have multiple servers running your application, or do not
need the extra features that memcached offers then APCu is probably your best choice for object caching.

network configuration တစ္ခုတည္းမွာဆိုရင္ APCu က memcached နဲ့ ယွဥ္ရင္ access speed ပိုသာျပီး memcached က scale up လုပ္မယ္ဆို ပိုျမန္ပါတယ္။ သင့္ရဲ့ application က server မ်ားမ်ား ရွိဖို့ မလိုအပ္ဘူးဆိုရင္ ဒါမွမဟုတ္ memcached မွ ရနိုင္တဲ့ feature ေတြထက္ ပိုမလိုအပ္ဘူးဆိုရင္ APCu က object caching လုပ္ဖို့ အေကာင္းဆံုးေရြးခ်ယ္မွု ျဖစ္ေကာင္းျဖစ္နိုင္ပါတယ္။

Example logic using APCu:
APCu သံုးထားတဲ့ logic ဥပမာ

{% highlight php %}
<?php
// check if there is data saved as 'expensive_data' in cache
$data = apc_fetch('expensive_data');
if ($data === false) {
    // data is not in cache; save result of expensive call for later use
    apc_add('expensive_data', $data = get_expensive_data());
}

print_r($data);
{% endhighlight %}

Note that prior to PHP 5.5, APC provides both an object cache and a bytecode cache. APCu is a project to bring APC's
object cache to PHP 5.5+, since PHP now has a built-in bytecode cache (OPcache).

### Learn more about popular object caching systems:

* [APCu](https://github.com/krakjoe/apcu)
* [APC Functions](http://php.net/ref.apc)
* [Memcached](http://memcached.org/)
* [Redis](http://redis.io/)
* [XCache APIs](http://xcache.lighttpd.net/wiki/XcacheApi)
* [WinCache Functions](http://php.net/ref.wincache)
