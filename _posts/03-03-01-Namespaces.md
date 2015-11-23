---
isChild: true
anchor:  namespaces
---

## Namespaces {#namespaces_title}

အထက်မှာဖော်ပြခဲ့သလိုဘဲ PHP community မှာ developers တွေအများကြီးက code တွေအများကြီးကို create လုပ်နေကြတယ်။ ဒါကဘာကိုဆိုလိုတာလဲဆိုရင် PHP library ထဲက code တွေထဲက class name တစ်ခုကအခြား library မှာလည်းရှိနိုင်တာကိုပြောချင်တာပါ။ libraries နှစ်ခုလုံးက namespace တစ်ခုတည်းကိုသုံးတဲ့အခါမှာ အဲ့ဒါတွေက code တွေကိုထိခိုက်ပြီးတော့ ပြဿနာတက်ကုန်ပါတယ်။

_Namespaces_ တွေကအဲ့ဒီ့ပြဿနာတွေကိုဖြေရှင်းပေးတာပါ။  PHP reference manual ထဲမှာဖော်ပြထားတဲ့အတိုင်းဆိုရင်၊ namespaces တွေကို operating system directories တွေနဲ့နှိုင်းယှဉ်ရပါလိမ့်မယ်၊ အဲ့ဒီ့ _namespace_ files; တွေက အမည်အတူတူနဲ့မတူညီတဲ့ directories ထဲမှာတည်ရှိနိုင်ပါတယ်။ ထိုနည်းတူဘဲ PHP classes နှစ်ခုက အမည်အတူတူနဲ့ မတူညီတဲ့ namespaces ထဲမှာတည်ရှိနိုင်ပါတယ်။ ဒါကတော့ရှင်းရှင်းလေးပါဘဲ။

သင့် code ကို namespace လုပ်ဖို့သင့်အတွက်အရေးကြီးပါတယ် ဘာလို့လည်းဆိုရင် အခြား developer တွေကသင့်ဆီက code ကိုအခြား libraries တွေနဲ့မညိဘဲအသုံးပြုနိုင်ပါလိမ့်မယ်။

namespace ကို [PSR-4][psr4] မှာဖော်ပြခဲ့တဲ့အတိုင်း အသုံးပြုဖို့ရာအတွက် ထောက်ခံမှူတစ်ခုလုပ်ချင်ပါတယ်၊ အဲ့ဒါရဲ့ရည်ရွယ်ချက်ကတော့ standard file ၊ class နဲ့ namespace convention တွေကို plug-and-play code ဖြစ်စေဖို့ရာအတွက်ဘဲဖြစ်ပါတယ်။

October 2014 မှာ PHP-FIG က အရင် autoloading standard: [PSR-0][psr0] ကို deprecate ဖြစ်သွားပြီးအဲ့ဒါကို [PSR-4][psr4] နဲ့အစားထိုးလိုက်ပါတယ်။ လက်ရှိမှာတော့ နှစ်ခုလုံးကအသုံးဝင်ပါသေးတယ်၊ PSR-4 က PHP 5.3 လိုအပ်ပြီးတော့ PHP 5.2 ကိုသုံးပြုတဲ့များစွာသော project တွေကတော့ PSR-0 ကိုအသုံးပြုဆဲပါဘဲ။ သင့် application အသစ် ဒါမှမဟုတ် package အတွက် autoloader standard သုံးမယ်ဆိုရင်တော့ PSR-4 ကိုသင်သေချာပေါက်ကြည့်ချင်ပါလိမ့်မယ်။

* [Read about Namespaces][namespaces]
* [Read about PSR-0][psr0]
* [Read about PSR-4][psr4]


[namespaces]: http://php.net/language.namespaces
[psr0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
[psr4]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md
