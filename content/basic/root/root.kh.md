---
title: "ព័ត៌មានពី Root"
date: 2019-09-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
draft: false
# search related keywords
keywords: ["induct", "instate"]
---
**root** គឺជាឈ្មោះអ្នកប្រើ រឺគណនីដែលអាចចូលប្រើរាល់ពាក្យបញ្ជានិងឯកសារទាំងអស់នៅលើប្រព័ន្ធ  LINUX រឺក៏ដូចជាប្រព័ន្ធប្រតិបត្តការគម្ពីរ​។ ការចូលប្រើជាញឹកញាប់គឺចាំបាច់សម្រាប់ដំណើរការពាក្យបញ្ជានៅក្នុងប្រព័ន្ធ ជាពិសេសពាក្យបញ្ជាដែលប៉ះពាល់ដល់ឯកសារប្រព័ន្ធ។  root មានឥទ្ធិពលខ្លាំងវាត្រូវបានអនុញ្ញាតឱ្យ​ស្នើសុំ ការ ចូលទៅកាន់ ផ្នែកសំខាន់។​  នៅពេលចាំបាច់ទើបអ្នកប្រើប្រាស់ root ។ នេះអាចជួយការពារការបំផ្លាញឯកសារ ប្រព័ន្ធសំខាន់ៗ។

---
---

### ការចូល​ Root តាម​កុនសូល
ប្រសិនបើអ្នកមានបំណងចង់ចូលអ្នកជា **"អ្នកប្រើជាន់ខ្ពស់"** អ្នកពិតជាអាចប្រើពាក្យបញ្ជានេះដើម្បីចូលជា អ្នកប្រើប្រាស់ណាមួយនៅលើម៉ាស៊ីន។

```
su -
``` 
{{< notice note >}}
ពាក្យសម្ងាត់របស់អ្នកត្រូវបានទាមទារសម្រាប់ចូលជា root ។ សូមប្រាកដថាបញ្ចូលលេខសំងាត់របស់​ អ្នកអោយបានត្រឹមត្រូវ ពីព្រោះនៅពេលដែល​អ្នកវាយបញ្ចូលវាមិនត្រូវបានបង្ហាញលើអេក្រង់ទេ។
{{< /notice >}}


នៅពេលដែលអ្នកចូលជា **root** ប្រអប់បញ្ចូលពាក្យបញ្ជាគួរតែបញ្ចប់និមិត្តសញ្ញាដូចនេះ៖
- `$` --- មានន័យថាអ្នកមិននៅក្នុងroot។
- `#` --- មានន័យថាអ្នកកំពុងនៅក្នុង​ root។

នេះជាឧទាហរណ៍៖
**ក្រៅ​ Root**
```
koompi@koompi-os$~ 
```
**ក្នុង Root**
```
root@koompi-os ~ #  
```
### ការចាកចេញពី Root
អ្នកអាច **ចាកចេញពី​​ Root** តាមពីររបៀប:

**+ របៀបទីមួយ, បញូ្ខល:**
```
exit
```
**+ របៀបទីពីរ,​បញ្ចូល:**
```
logout
```
### កំណត់ ឬកំណត់លេខសំងាត់ឡើងវិញ
ប្រសិនបើអ្នកភ្លេចលេខកូដសំងាត់​ និងលេខសម្ងាត់អ្នកប្រើប្រាស់របស់អ្នក អ្នកត្រូវចូលទៅក្នុង Boot របៀបស្តារ ឡើងវិញ​និង ដើម្បីផ្លាស់ប្តូរវា។ 

ប្រសិនបើអ្នកដឹងពីលេខសម្ងាត់អ្នកប្រើប្រាស់របស់អ្នក ហើយត្រូវការផ្លាស់ប្តូរលេខសម្ងាត់ ជាថ្មី អ្នកគ្រាន់តែ វាយពាក្យ `sudo passwd` បញ្ចូលពាក្យសំងាត់អ្នកប្រើប្រាស់ បន្ទាប់មកបង្កើតលេខសំងាត់ថ្មី។
 
```
sudo password root
```
### ចាក់សោរ និងដោះសោរ Root
ប្រសិនបើអ្នកចង់ចាក់សោរគណនី root សូមបញ្ចូលពាក្យបញ្ជាខាងក្រោមដើម្បីដកលេខសម្ងាត់​ ហើយចាក់សោរ root៖
```
sudo passwd -dl root
```
ប្រសិនបើអ្នកចង់ដោះសោគណនី root សូមបញ្ចូលពាក្យបញ្ជាខាងក្រោម ដើម្បីកំណត់លេខសំងាត់ថ្មីហើយដោះសោរវា៖
```
sudo passwd root
```
{{< notice note >}}
អ្នកនឹងត្រូវបានសួរឱ្យបង្កើតពាក្យសម្ងាត់ថ្មីហើយបញ្ចូលវាពីរដង។ នៅពេលដែលពាក្យសម្ងាត់ត្រូវបានកំណត់គណនី root នឹងបានបើក។
{{< /notice >}}

----
----