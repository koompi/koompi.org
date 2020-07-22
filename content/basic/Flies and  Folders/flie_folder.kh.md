---
title: "ព័ត៌មានពី Files/Folders"
date: 2019-11-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
draft: false
# search related keywords
keywords: ["induct", "instate"]
---

ផ្នែកនេះគឺជាការណែនាំសម្រាប់ព័ត៌មានទាក់ទងនឹង **ឯកសារនិងថតឯកសារ (Files/Folders)** ។ ពាក្យបញ្ជា ទាំងអស់នឹងត្រូវបានផ្តល់នៅទីនេះជាមួយនឹងការពន្យល់ព្រមទាំងឧទាហរណ៍ផងដែរ។

សម្រាប់ព័ត៌មានលម្អិតនៃការណែនាំសូមមើលអត្ថបទនៅ [គេហទំព័រ KOOMPI OS ](www.koompi.org) ឬអត្ថបទ[ផ្នែកកម្មវិធីផ្សេងៗ](www.koompi.org/applications/) ដែលភ្ជាប់ជាមួយសៀវភៅណែនាំ។

---
---

## ការបង្កើត File
ការដឹងពីរបៀបបង្កើតឯកសារថ្មី **(File)** គឺជារឿងដ៏សំខាន់សម្រាប់ អ្នកដែលប្រើប្រាស់ Open-Source។ អ្នកអាច បង្កើតឯកសារថ្មី `បន្ទាត់បញ្ជា` ឬពី `កម្មវិធីគ្រប់គ្រងឯកសារលើកុំព្យូទ័រ` ។

ពាក្យបញ្ជា `touch` អនុញ្ញាតឱ្យយើងធ្វើការកែប្រែលើឯកសារនិងថតដែលមានស្រាប់ក៏ដូចជា ការបង្កើតឯកសារ ផងដែរ។ មធ្យោបាយដែលងាយស្រួល និងចងចាំបំផុតតែមួយគត់ ដើម្បីបង្កើតឯកសារទទេ គឺដោយការប្រើ `touch`។

ដើម្បីបង្កើតឯកសារថ្មីគ្រាន់តែដំណើរការពាក្យបញ្ជា touch ហើយដាក់ឈ្មោះឯកសារដែលអ្នកចង់៖
```
touch Files_Name.txt
```
អ្នកក៏អាចបង្កើតឯកសារពីរ ឫច្រើនក្នុងពេលតែមួយផងដែរ៖
```
 touch File_Name1.txt File_Name2.txt File_Name3.txt
```

{{< notice info >}}
`.txt`សម្គាល់ឯកសារជាអត្ថបទ។ អ្នកក៏អាចប្រើ`ផ្នែកបន្ថែមផ្សេងទៀត`សម្រាប់សម្គាល់ប្រភេទឯកសារដែលអ្នក ចង់ប្រើផងដែរ។
{{< /notice >}}

ក្រៅពី `touch`, អ្នកក៏អាចប្រើ`អេកូ` ដើម្បីបង្កើតឯកសារផងដែរ។ ពាក្យបញ្ជា `អេកូ` បង្ហាញ **ទិន្នន័យជាតួអក្សរ** ដែលត្រូវបានបញ្ជូនទៅជាលទ្ធផលក្នុងការបង្ហាញ។
```
 echo "some line" >> File_Name.txt
```
ឧទាហរណ៍៖
```
 echo $null >> sample.txt
```
{{< notice note >}}
`$null` សម្គាល់ថា ទេ នៅទីនេះ។
{{< /notice >}}
## ការលុប File
ការលុបឯកសារ គឺជាផ្នែកមួយនៃប្រតិបត្តិការដែលធ្វើឡើងជាញឹកញាប់ដោយពាក្យបញ្ជា `rm` ជាមួយឈ្មោះឯកសារដែលអ្នកចង់លុបចេញ៖
```
rm File_Name
```
នេះជាឧទាហរណ៍៖
```
rm sample.txt 
```

## ការបង្ហាញអត្តបទ
ពាក្យបញ្ជា **cat** ត្រូវបានប្រើជាញឹកញាប់ វាធ្វើការអានទិន្នន័យពីឯកសារនិងការបង្ហាញ។ វាជួយយើងក្នុងការបង្កើត និងមើល។
```
 cat File_Name
```
## ការកែប្រែ File
ក្នុងប្រព័ន្ធប្រតិបតិ្ថការមានវិធីជាច្រើន ដើម្បីកែឯកសារតាមរយៈពាក្យបញ្ជាដូចជា vi, emacs, pico, ed និង nano ។ ក្នុងចំណោមពាក្យបញ្ជាទាំងនោះមានតែ nano ដែលកំពុងប្រើជាប្រចាំ។
```
nano File_Name
```
{{< notice note >}}
ពេលខ្លះយើងត្រូវបន្ថែម `ពាក្យបញ្ជា sudo`ដែលតំណាងឱ្យ **superuser** នៅពីមុខវាដើម្បីកែសម្រួល *Files* មួយចំនួន។
{{< /notice >}}
```
sudo nano File_Name
```
## ការថតចម្លង File និង Folder
ឧទាហរណ៍ងាយៗពីពាក្យបញ្ជា cp ក្នុងការថតតចម្លង files (ដោយ file ដើមមិនប្រែប្រួល៖
```
 cp File_Name NewFile_Name
```
ប្រសិនបើអ្នកចង់ចម្លង File ពីថតមួយទៅថតមួយ អ្នកអាចប្រើតាមរបៀបខាងក្រោម៖
```
cp -R <source_folder> <destination_folder>
```
### ជម្រើសដទៃ
`-i`សម្រាប់អន្តរកម្មដោយសួរអ្នក ដើម្បីបញ្ជាក់ថាតើឯកសារមានស្រាប់ ត្រូវបានសរសេរកែប្រែពីលើនៅក្នុង ដំណើរការចម្លង។

`-r` សម្រាប់ការចម្លងថតរងនិងឯកសារទាំងអស់នៅក្នុងថតឯកសារដើម។

`-v` បង្ហាញឯកសារដែលត្រូវបានចម្លងម្តងមួយៗ។

## ការប្តូរទីតាំង file or folder
ដើម្បីស្វែងរកនិងផ្លាស់ទីថតអាចធ្វើតាមការណែនាំខាងក្រោម៖
```
mv Folder_Name NewFolder_Name
```
## ការបង្កើត Folder
we can create directories from command line using the command `mkdir`. Syntax of this command is explained below.
```
 mkdir Folder_Name
```
For example, to create a folder named ‘newfolder‘ the command is:
```
 mkdir NewFolder
```
## Remove Folder
Removing folder is like removing the file, too but it has a little bit different. You have to add `-r` after `rm command`.
```
 rm -r Folder_Name
```
## List Folder Contents
Listing Command (ls) allows us to see all the contents in the directory we are in.
```
 ls
```
### Options
| Options  | Descriptions| 
|:-------------|:-------------|
| **ls -a**|      `list all files including hidden file starting with '.'`|
| **ls --color** |      `colored list [=always/never/auto]`|
| **ls -d** |       `list directories - with ' */'`|
| **ls -F** |       `add one char of */=>@| to enteries`|
| **ls -i**|       `list file's inode index number`|
| **ls -l** |      `list with long format - show permissions`|
| **ls -la** |   `list long format including hidden files` |
| **ls -lh** |   `list long format with readable file size` |
| **ls -ls** |   `list with long format with file size` |
| **ls -r** |   `list in reverse order` |
| **ls -R** |   `list recursively directory tree` |

For more info use `--help` after the command like this `ls --help``.
## Change Folder or Directory
`cd` is the command for changing the folder/directory of the command line. Here its syntax:
```
 cd Folder_Name
```
Changing to home directory (determined by $HOME environment variable):
```
 cd
```
Also change to home directory:
```
 cd .
```
Change to parent directory:
```
 cd ..
```
Change to subdirectory Documents:
```
 cd Documents
```
Change to directory with absolute path
```
 cd path1/path2/path3
```
Change to directory name with white space -*path Name*
```
 cd path\ Name 
```
{{< notice tip >}}
`\` here is stand for white space !!!
{{< /notice >}}
## Show Current Folder
To show the directory you are currently in:
```
 pwd
```
**Output :**
```
 /home/koompi
```
## Create Physical Link to File or Folder
To make links between files you need to use `ln` command. A symbolic link (also known as a soft link or symlink) consists of a special type of file that serves as a reference to another file or directory.
```
ln [FileName] [LinkName]
```
## Find Phrase Within File
The grep command is used to search text. It searches the given file for lines containing a match to the given strings or words. It is one of the most useful commands.

Below is some standard grep command explained with examples to get you started with grep. Search any line that contains the word in filename.
```
 grep 'Strings' FileName
```
Perform a case-insensitive search for the word:
```
 grep -i 'Strings' FileName
```
Looking for all files in the current directory and in all of its subdirectories.
```
 grep -R 'Strings'
```
Searching and displaying the total number of times that the string appears in FileName.
```
 grep -c 'Strings' FileName
```
Searching by paths:
```
 grep 'Strings' path/path/path
```

## Mount Filesystem
You can mount the filesystem with the syntax below:
```
 mount /dev/[device] [path]
```
## Unmount Filesystem
You can also unmount filesystem with command below.
```
 unmount [path]
```
## Make File Executable
Change the rights to a file so that it can run as a program.
```
 chmod +x filename
```
## List Trash Files
As you have already known what is `ls`  command, you should know the path of the trash file.
```
 ls -l files ~/.local/share/Trash/files
```
## Empty Trash
Above are the paths of trash file, we can empty it with `rm -r` command:
```
 rm -r ~/.locale/share/Trash
```

---
---



