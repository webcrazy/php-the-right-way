---
isChild: true
anchor:  command_line_interface
---

## Command Line Interface {#command_line_interface_title}


PHP ဟာ web applications တွေဖန်တီးဖို့အတွက် create လုပ်ခဲ့ခြင်းဖြစ်ပါတယ်။ ဒါပေမယ့် PHP ဟာ command line interface (CLI) programs တွေအတွက်လည်း အသုံးဝင်ပါတယ်။
Command line PHP Programs တွေက ယျေဘူယျ automate task တွေကို အထောက်အကူပြုပါတယ်။  ဥပမာ testing တို့ development နဲ့ application ကိုထိန်းသိမ်းရန် တို့လိုပေါ့။

CLI PHP programs တွေဟာ powerful ဖြစ်ပါတယ်၊ အကြောင်းက သင့် app ရဲ့ code ကို secure web GUI လုပ်စရာမလိုဘဲ တိုက်ရိုက် အသုံးပြုလို့ရတာကြောင့်ပါ။ **သတိပြုရန်** ကတော့ သင့်ရဲ့ CLI PHP scripts တွေကို public web root မှာ မထားဖို့ပါဘဲ။

PHP ကို command line ကနေ run လိုပါက 

{% highlight console %}
> php -i
{% endhighlight %}

`-i` option က သင့်ရဲ့ PHP configuration ကို command line မှာဖော်ပြပေးမှာဖြစ်ပါတယ် [`phpinfo()`][phpinfo] function လိုပါဘဲ။

`-a` option ကတော့ interactive shell ပါ, Ruby ရဲ့ IRB နဲ့ Python ရဲ့ interactive shell နဲ့အတူတူပါဘဲ။ အခြား အသုံးဝင်တဲ့ [command line options](cli-options)  တွေလည်းရှိပါတယ်။

Simple "Hello, $name" CLI program လေးတစ်ခုလောက်ရေးလိုက်ကြအောင်။ အဲ့ဒါကိုရေးဖို့ `hello.php` ဆိုတဲ့ file တစ်ခု create ပြီး အောက်မှာဖောပြထားတဲ့အတိုင်းရေးလိုက်ပါ

{% highlight php %}
<?php
if ($argc !== 2) {
   echo "Usage: php hello.php [name].\n";
   exit(1);
}
$name = $argv[1];
echo "Hello, $name\n";
{% endhighlight %}


PHP က special variables နှစ်ခု ကို သင့် script argument run လိုက်တဲ့အပေါ်မူတည်ပြီးတော့ sets up လုပ်လိုက်ပါတယ်။
 [`$argc`][argc] က  integer variable တစ်ခုဖြစ်ပြီးတော့ argument *count* နဲ့ [`$argv`][argv] က array variable တစ်ခုဖြစ်ပြီး argument တစ်ခုချင်းဆီရဲ့ **value** ပါဝင်ပါတယ်။ ပထမ argument ကသင့် PHP script file name ဖြစ်ပါတယ်၊ အခုအခြေအနေမှာဆိုရင် `hello.php` ဖြစ်ပါတယ်။


`exit()` expression က 0 မဟုတ်တဲ့ numbers တွေကို ယျေဘူယျအားဖြင့် command failed ဖြစ်တယ်ဆိုတာကို shell ကသိဖို့ရာအတွက်အသုံးပြုပါတယ်။ exit codes တွေကို [ဒီမှာ](exit-codes) တွေ့နိုင်ပါတယ်။

ထက်မှာဖော်ပြထားတဲ့ script ကို command line ကနေ run ဖို့အတွက်:

{% highlight console %}
> php hello.php
Usage: php hello.php [name]
> php hello.php world
Hello, world
{% endhighlight %}

 * [PHP ကို command line မှ run တာကိုလေ့လာခြင်း][php-cli]
 * [Window မှာ command line ဘယ်လို run မလဲဆိုတာလေ့လာခြင်း][php-cli-windows]


[phpinfo]: http://php.net/function.phpinfo
[cli-options]: http://php.net/features.commandline.options
[argc]: http://php.net/reserved.variables.argc
[argv]: http://php.net/reserved.variables.argv
[exit-codes]: http://www.gsp.com/cgi-bin/man.cgi?section=3&amp;topic=sysexits
[php-cli]: http://php.net/features.commandline
[php-cli-windows]: http://php.net/install.windows.commandline
