لوپس تمام جدید پروگرامنگ زبانوں میں ایک مفید اور کثرت سے استعمال ہونے والی خصوصیت ہیں۔

اگر آپ کسی مخصوص تکرار والے کام کو خودکار بنانا چاہتے ہیں یا اپنے آپ کو اپنے پروگراموں میں تکرار کا کوڈ لکھنے سے روکنا چاہتے ہیں تو ، لوپ کا استعمال اس کے لئے بہترین آپشن ہے۔

لوپ ہدایات کا ایک مجموعہ ہے جو کسی شرط کو پورا کرنے تک بار بار چلتا ہے۔ آئیے اس بارے میں مزید جانیں کہ پائتھن میں لوپ کس طرح کام کرتے ہیں۔

## پائتھن میں لوپ
پائتھن میں دو قسم کے لوپس بنائے گۓ ہیں:


- `for` لوپس
- `while` لوپس

آئیے اس بات پر توجہ مرکوز کریں کہ آپ پائتھن میں `while` لوپ کو کیسے بنا سکتے ہیں اور یہ کیسے کام کرتا ہے۔

## پائتھن میں وائل لوپ کیا ہے؟


پائتھن میں while loop کا عام سنٹیکس اس طرح نظر آتا ہے:

```{python}
while condition:
    execute this code in the loop's body
```

وائل لوپ کوڈ کا ایک ٹکرا چلاے گا جبکہ ایک شرط برقرار رہے گی. یہ کوڈ پر اس وقت تک عمل کرتا رہے گا جب تک شرط درست رہتی ہے۔
وائل لوپ ہمیشہ چلنے سے پہلے شرط کو چیک کرے گا۔
اگر شرط `True` ہے تو لوپ، لوپ باڈی میں موجود کوڈ چلے گا۔
مثال کے طور پر، یہ لوپ تب تک چلتا رہے گا جب تک  `number` دس سے کم ہو:

```{python}
number = 0
while number < 10:
    print(f"Number is {number}!")
    number = number + 1
```

نتیجہ:

```{python}
Number is 0!
Number is 1!
Number is 2!
Number is 3!
Number is 4!
Number is 5!
Number is 6!
Number is 7!
Number is 8!
Number is 9!
```


یہاں، ویری ایبل `number` کو ابتدائی طور پر` 0` پر سیٹ کیا گیا ہے۔

کسی بھی کوڈ کو چلانے سے پہلے ، پائتھن شرط کی جانچ پڑتال کرتا ہے (`number < 10`)۔ یہ جانچتا ہے کہ شرط درست ہے، تو پرنٹ اسٹیٹمنٹ پر عمل درآمد ہوتا ہے اور  `Number is 0!` کنسول پر پرنٹ کیا جاتا ہے۔

اس کے بعد `number` میں `1` کا اضافہ کیا جاتا ہے۔ پھر دوبارہ جائزہ لیا جاتا ہے اور یہ دوبارہ درست ہے تو، پورا طریقہ کار اس وقت تک دہرایا جاتا ہے جب تک کہ  `number` `9`  کے برابر نہ ہو جائے۔

اس بعد `!number is 9` پرنٹ کیا جاتا ہے اور `number` میں اضافہ ہوتا ہے، لیکن اب `number` 10 کے برابر ہے لہذا شرط اب پوری نہیں ہوتی ہے اور اس وجہ سے لوپ ختم ہو جاتا ہے۔
یہ ممکن ہے کہ `while` لوپ کبھی نہیں چلتا ہے اگر یہ شرط کو پورا نہیں کرتا ہے، جیسا کہ اس مثال میں:

```{python}
number = 50
while number < 10 :
    print(f"Number is {number}!")
```


چونکہ یہ حالت ہمیشہ غلط ہوتی ہے، اس لیے لوپ کے باڈی میں دی گئی ہدایات پر عمل نہیں ہوتا ہے۔

## لامحدود لوپس نہ بنائیں
جیسا کہ آپ نے اوپر کی مثال میں دیکھا، `while` لوپس عام طور پر ایک متغیر کے ساتھ ہوتے ہیں جس کی قدر لوپ کی پوری مدت میں تبدیل ہوتی رہتی ہے۔ اور یہ بالآخر طے کرتا ہے کہ لوپ کب ختم ہوگا۔

اگر آپ اس لائن کو شامل نہیں کرتے ہیں، تو آپ ایک لامحدود لوپ بنائیں گے۔
`number` میں اضافہ اور اپ ڈیٹ نہیں کیا جائے گا۔ یہ ہمیشہ سیٹ رہے گا اور صفر پر رہے گا اور اس لیے شرط،  `number < 10` ہمیشہ کے لیے درست رہے گا۔ اس کا مطلب ہے کہ لوپ ہمیشہ کے لیے چلتا رہے گا۔

```{python}

# don't run this

number = 0
while number < 10:
    print(f"Number is {number}!")
```

نتیجہ: 
```{python}
Number is 0!
Number is 0!
Number is 0!
Number is 0!
Number is 0!
Number is 0!
Number is 0!
...
```

یہ لامحدود چلتا رہے گا۔

یہ ایسا ہی ہے جیسا کہ یہ کرنا:
```{python}

#don't run this
while True:
    print("I am always true")
```

اگر آپ خود کو اس طرح کی صورتحال میں پاتے ہیں تو کیا ہوگا؟

لوپ کو ختم کرنے کیلئے  `Control C ` دبائیں.

## do-while لوپ کیا ہے؟

دوسری پروگرامنگ زبانوں میں `do while` لوپ کا عمومی سنٹیکس کچھ اس طرح نظر آتا ہے:
```{python}
do {
  loop block statement to be executed;
  }
while(condition);
```


مثال کے طور پر، C لینگویج میں do while لوپ اس طرح لگتا ہے:
```{c}
#include <stdio.h>
 
int main(void)
 {
   int i = 10;
   do {
      printf("the value of i: %i\n", i);
      i++;
      }
  while( i < 20 );
 }
```
ڈو-وائیل لوپ میں جو چیز منفرد ہے وہ یہ ہے کہ لوپ بلاک میں موجود کوڈ کو کم از کم ایک بار عمل میں لایا جائے گا۔

سٹیٹمنٹ میں موجود کوڈ ایک بار چلتا ہے اور پھر کوڈ پر عمل درآمد کے بعد ہی  شرط (کنڈیشن) چیک کی جاتی ہے۔

لہذا کوڈ پہلے ایک بار چلتا ہے اور پھر کنڈیشن کی جانچ پڑتال کی جاتی ہے۔

اگر جانچ کی گئی کنڈیشن درست ہو، تو لوپ جاری رہتا ہے۔

ایسے معاملات ہیں، جہاں آپ چاہتے ہیں کہ آپ کا کوڈ کم از کم ایک بار چلے، اور یہ وہ جگہ ہے جہاں `do` لوپس کام آتے ہیں۔

مثال کے طور پر، جب آپ کوئی ایسا پروگرام لکھ رہے ہیں جو صارفین سے ان پٹ لیتا ہے  آپ صرف ایک مثبت نمبر مانگتے ہیں۔ کوڈ کم از کم ایک بار چلے گا۔ اگر صارف کی جمع کردہ تعداد منفی ہے، تو لوپ چلتا رہے گا۔ اگر یہ مثبت ہے تو یہ رک جائے گا۔
پائتھن میں دوسری زبانوں کی طرح واضح طور پر `do-while` لوپ بنانے کے لیے پہلے سے تیارشدہ فعالیت (functionality) نہیں ہے۔ لیکن پائتھن میں `do-while` لوپ کی تقلید کرنا ممکن ہے۔

## پائتھن میں do-while لوپ کی تقلید کیسے کریں۔

 پائتھن میں `do while` loop بنانے کے لیے، آپ کو `while` لوپ میں تھوڑا سا ترمیم کرنے کی ضرورت ہے تاکہ دوسری زبانوں کے `do while` لوپ جیسا برتاؤ حاصل کیا جا سکے۔

اب تک ریفریشر کے طور پر، ایک `Do while` لوپ کم از کم ایک بار چلے گا۔ اگر شرط پوری ہو جائے تو پھر چلے گا۔

دوسری جانب `while` لوپ کم از کم ایک بار نہیں چلتا ہے اور حقیقت میں کبھی نہیں چل سکتا ہے۔ یہ اس وقت چلتا ہے جب صرف شرط پوری ہوتی ہے۔
تو، ہم کہتے ہیں کہ ہمارے پاس ایک مثال ہے جہاں ہم چاہتے ہیں کہ کوڈ کی ایک لائن کم از کم ایک بار چلے۔
```{python}
secret_word = "python"
counter = 0

while True:
    word = input("Enter the secret word: ").lower()
    counter = counter + 1
    if word == secret_word:
        break
    if word != secret_word and counter > 7: 
        break
```

کوڈ کم از کم ایک بار چلے گا، صارف سے ان پٹ کے لیے پوچھے گا۔

یہ ہمیشہ `True` کے ساتھ کم از کم ایک بار چلنے کی ضمانت دیتا ہے، جو بصورت دیگر ایک لامحدود لوپ بناتا ہے۔

اگر صارف صحیح خفیہ لفظ داخل کرتا ہے، تو لوپ ختم ہو جاتا ہے۔

اگر صارف 7 سے زیادہ بار غلط خفیہ لفظ داخل کرتا ہے، تو لوپ مکمل طور پر ختم ہو جائے گا۔
 
بریک (`break`) سٹیٹمنٹ وائیل (`while`) لوپ کے بہاؤ کو کنٹرول کرنے کی اجازت ڈیتا ہے اور لامحدود لوپ کے ساتھ ختم نہیں ہو جاتا.

(`break`)  بریک فوری طور پر موجودہ لوپ کو ایک ساتھ ختم کر دے گا اور اس سے باہر نکل جائے گا۔

تو اس طرح سے آپ پائتھن میں `do while` لوپ سے ملتا جلتا اثر بناسکے ہیں۔

لوپ ہمیشہ کم از کم ایک بار چلتا ہے۔ اگر شرط پوری نہیں ہوتی ہے تو یہ لوپ جاری رکھے گا اور پھر شرط پوری ہونے پر ختم ہو جائے گا۔

## نتیجہ

اب آپ جانتے ہیں کہ پائتھن میں کیسے آپ `do while` لوپ بنانا ہے.

اگر آپ پائتھن کے بارے میں مزید جاننے میں دلچسپی رکھتے ہیں، تو آپ freeCodeCamp کے یوٹیوب چینل پر 12 پائتھن پروجیکٹس کی ویڈیو دیکھ سکتے ہیں۔ آپ کو 12 پروجیکٹس بنانے کا موقع ملے گا اور یہ ابتدائی افراد کے لیے تیار ہے۔

freeCodeCamp کے پاس ایک مفت پائتھن سرٹیفیکیشن بھی ہے جو آپ کو پائتھن کے ضروری بنیادی اصولوں کی اچھی سمجھ اور ایک اچھی طرح سے جائزہ لینے میں مدد کرتا ہے۔