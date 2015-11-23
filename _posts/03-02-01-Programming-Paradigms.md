---
isChild: true
anchor:  programming_paradigms
---

## ပရိုဂရမ်ရေးသား　ဟန်များ  {#programming_paradigms_title}

PHP ဟာ ပရိုဂရမ်ရေးသားနည်းမျိုးကွဲများစွာကို ပံ့ပိုးပေးထားတဲ့ အသုံးပြုရလွယ်ကူတဲ့ ဒိုင်းနမစ် ပရိုဂရမ်ဘာသာစကားတစ်ခုဖြစ်ပါတယ်။ PHP ရဲ့ နှစ်များစွာကြာတဲ့ သက်တမ်းတစ်လျှောက် သိသိသာသာပြောင်းလဲခဲ့ပါတယ်။　မှတ်သားဖွယ်ပြောင်းလဲမှုတွေကတော့ ၂၀၀၄ ခုနှစ် PHP 5.0 မှာ Object တွေကို အခြေခံတဲ့ ပရိုရမ်ရေးသားနည်း  ပုံစံ ကို ခိုင်ခိုင်မာမာ ထည့်သွင်းခဲ့တာ၊ ၂၀၀၉ ခုနှစ် PHP 5.3 မှာ  Anonymous Function နဲ့　Name Space တွေထည့်သွင်းခဲ့တာ၊ ၂၀၁၂ ခုနှစ် PHP 5.4 မှာ traits တွေထည့်သွင်းခဲ့တာတွေ ပဲဖြစ်ပါတယ်။


### Object ဗဟိုပြုပရိုဂရမ်ရေးသားခြင်း

PHP မှာ Object ဗဟိုပြုပရိုဂရမ်ရေးသားခြင်း အတွက် ပြည့်စုံတဲ့ ပံ့ပိုးမှုတွေ ပါ၀င်ပါတယ်။ class များ၊ abstract class များ၊ interface များ၊ inheritance၊ constructor များ၊ cloning၊ exception နဲ့ အခြားသော ပံ့ပိုးမှုတွေဖြစ်ပါတယ်။

* [Object-oriented PHP အကြောင်းဖတ်ရန်][oop]
* [Trait များအကြောင်းဖတ်ရန်][traits]

### Function ဗဟိုပြု ပရိုဂရမ်ရေးသားခြင်း

PPHP ဟာ first class  function တွေကို အထောက်အပံ့ပေးတဲ့အတွက် function တစ်ခုကို variable တစ်ခုအတွင်းမှာ ထည့်သုံးလို့ရပါတယ်။
User သတ်မှတ်ပေးတဲ့ function တွေရော၊ မူလပါ၀င်ပြီးသား function တွေကိုပါ variable တစ်ခုအတွင်းမှာ ထည့်သွင်းမှတ်သားပြီး  လိုသလိုခေါ်ယူသုံးနိုင်ပါတယ်။
function တွေကို အခြား function တွေရဲ့ argument အဖြစ်(higher order function လို့ခေါ်ပါတယ်။)ထည့်သွင်းပေးနိုင်သလို function တစ်ခုမှအခြား function တစ်ခုကိုလည်း return ပြန်ပေးလို့ရပါတယ်။

Recursion(function တစ်ခုမှ မိမိကိုယ်ကိုယ် ပြန်ခေါ်ယူအသုံးပြုခြင်း)ကိုလည်း အထောက်အပံ့ပေးထားပါတယ်။ ဒါပေမဲ့ PHP codeအများစုကတော့ iteration ကိုပဲ အာရုံစိုက်အသုံးပြုလေ့ ရှိပါတယ်။

PHP 5.3 (၂၀၀၉နှစ်)ကစလို့ closure အထောက်အပံ့ပါတဲ့ anonymous function တွေလည်းပါရှိနေပြီ ဖြစ်ပါတယ်။

PHP 5.4 မှာတော့ closure တွေကို object တစ်ခုရဲ့ scope အတွင်းမှာပဲ ချိတ်ဆက်ယူနိုင်တဲ့ စွမ်းရည်တွေ၊ anonymous function တွေနဲ့ကြိုက်သလိုအစားထိုး ပြောင်းလဲအသုံးပြုနိုင်အောင် callable တွေအတွက်ပိုမိုကောင်းမွန်တဲ့ အထောက်အပံ့တွေပါလာပါတယ်။

* [PHP နှင့် Function ဗဟိုပြု ပရိုဂရမ်ရေးသားခြင်းအကြောင်းဖတ်ရန်](/php-the-right-way/pages/Functional-Programming.html)
* [Anonymous Functions အကြောင်းဖတ်ရန်][anonymous-functions]
* [Closure class အကြောင်းဖတ်ရန်][closure-class]
* [Closures RFC အကြောင်းအသေးစိတ်ဖတ်ရန်][closures-rfc]
* [Callable များအကြောင်းဖတ်ရန်][callables]
* [`call_user_func_array()` အားသုံး၍ dynamic ခေါ်ယူနိုင်သော functionများအကြောင်းဖတ်ရန်][call-user-func-array]

### Meta Programming

PHP ဟာ Reflection API နဲ့ Magic Methods လိုနည်းလမ်း တွေကိုသုံးပြီး meta programming ပုံစံအမျိုးမျိုးကို အထောက်အပံ့ပေးထားပါတယ်။
`__get()`, `__set()`, `__clone()`, `__toString()`, `__invoke()` အစရှိတဲ့ magic methods တွေဟာအသုံးပြုတဲ့ developer ကို class တစ်ခုရဲ့ လုပ်ငန်းစဥ် အတွင်းကို ၀င်ရောက်ချိတ်ဆက်ပြုပြင်နိုင်ဖို့ ခွင့်ပြုပေးထားပါတယ်။ Ruby developerတွေက PHP မှာ `method_missing` မပါတာကို မကြာခဏ ပြောလေ့ရှိပေမဲ့ တကယ်တော့ `__call()` နဲ့ `__callStatic()` method တွေအဖြစ်ရှိပြီးသား ဖြစ်ပါတယ်။

* [Magic Method တွေအကြောင်းဖတ်ရန်][magic-methods]
* [Reflection အကြောင်းဖတ်ရန်][reflection]
* [Overloading အကြောင်းဖတ်ရန်][overloading]


[oop]: http://php.net/language.oop5
[traits]: http://php.net/language.oop5.traits
[anonymous-functions]: http://php.net/functions.anonymous
[closure-class]: http://php.net/class.closure
[closures-rfc]: https://wiki.php.net/rfc/closures
[callables]: http://php.net/language.types.callable
[call-user-func-array]: http://php.net/function.call-user-func-array
[magic-methods]: http://php.net/language.oop5.magic
[reflection]: http://php.net/intro.reflection
[overloading]: http://php.net/language.oop5.overloading

