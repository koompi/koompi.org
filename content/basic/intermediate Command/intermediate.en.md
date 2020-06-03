---
title: "Intermediate"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
draft: false
# search related keywords
keywords: ["induct", "instate"]
---




# Update Operating System
The **mandatory step** is to upgrade your operating system before downloading any new applications.


```
 pi -Syu
```
For Database Updates:
```
pi -Syy
```
# Installing Packages
Follow the following command to install a signal package including the dependencies:
```shell
     pi -S <Package name> or pi -i <Package name>
```
For the list of packages installation:
```shell
     pi -S <Package name1 Package name2 ...>
```
# Installing Package Group
Some packages belong to a **group of packages** that simultaneously call installation. As in here, for instance:


```shell
    pi -S <Package group name>
```
To see what inside the package group, run:
```shell
     pi -Sg <Package group name>
```
# Removing Packages
If you just want to remove the package, the command following will be enough:
```    
     pi -R <Package name>
```
To remove the package and those of its dependencies that aren’t needed by any other application, do:
```
     pi -Rs <Package name>
```
To remove a package, its dependencies and all the packages that depend on the target package:
```
     pi -Rsc <Package name>
```
 For deleting a package that other packages need without deleting their dependency package:

```
     pi -Rdd <Package name>
```
> **Note:** All operations have required a password. Then if you aren’t satisfied with the build tool and configuration choices, you can eject at any time. This command will remove the single build dependency from your operation.
{.is-info}


> **Tips:** Here Special usage to automate the install procedure (Recommend):
{.is-success}

```shell
 yes | pi -S <Package name> 
```
> **Tips:** Install packages with no confirm	
{.is-success}
```
 pi -S --noconfirm <Package name>
```


# Listing Packages
You may want to get the list of installed packages with their version, which is useful while reporting bugs or discussing installed packages.

- List all explicitly installed packages: `pi -Qe`.
List all packages in the **package group** named group: `pi -Sg group`
- List all explicitly installed native packages (i.e. present in the sync database) that are not direct or optional dependencies: `pi -Qent`.
- List all foreign packages (typically manually downloaded and installed or packages removed from the repositories): `pi -Qm`.
- List all native packages (installed from the sync database(s)): `pi -Qn`.
- List packages by regex: `pi -Qs regex`.
- List packages by regex with custom output format: `expac -s "%-30n %v" regex` (needs **expac**).

### Listing Changed Backup Files
If you want to backup your system configuration files you could copy all files in `/etc/`, but usually, you are only interested in the files that you have changed. Modified **backup files** can be viewed with the following command:
```
     pi -Qii | awk '/^MODIFIED/ {print $ 2}'
```

Running this command with root permissions will ensure that files readable only by root (such as /etc/sudoers) are included in the output.

### Listing All Changed Files From Packages
If you are suspecting file corruption (e.g. by software/hardware failure), but are unsure if files were corrupted, you might want to compare with the hash sums in the packages. 
```shell
     paccheck --md5sum --quiet
```

# Removing Unused Packages (orphans)
For recursively removing orphans and their configuration files:
```shell
     pi -Rns $ (pi -Qtdq)
```
If no orphans were found pacman outputs `error: no targets specified`. This is expected as no arguments were passed to `pi -Rns`.


# Backup The Pi Database
The following command can be used to back up the local pi database:
```
     tar -cjf pacman_database.tar.bz2 /var/lib/pacman/local
```
> **Noted**: If the **pi** database files are corrupted, and there is no backup file available, there exists some hope of rebuilding the pi database.
{.is-info}

# Reinstalling all packages
To reinstall all native packages, use:
```shell
 pi -Qqn | pi -S -
```
# Password Info 

Both **KOOMPI OS** and **Linux** operating systems use the `passwd` command to change the user password. The `passwd` is used to update a user’s authentication token (password) stored in `/etc/shadow file`. The `passwd` change passwords for user and group accounts. 
 
A normal user may only change the password for his/her own account, `the superuser (or root)` may change the password for any account. 


The **administrator** of a group may change the password for the group. It also changes account information, such as the full name of the user, user login shell, or password expiry date and interval.

### Set User Password
Type the following command to change your own password
```
 passwd
```
**Sample Output:**
```
    [koompi@koompi-pc ~]$ passwd
    Changing password for koompi.
    Current password: 
    New password: 
    Retype new password: 
    passwd: password updated successfully
```
The **user** is first prompted for his/her old password if one is present. This password is then encrypted and compared against the stored password. The user has only one chance to enter the correct **password**. 
 
**The superuser** is permitted to bypass this step so that forgotten passwords may be changed. **A new password** is tested for complexity. As a general guideline, passwords should consist of 10 `to` 20 `characters` including one or more** from each of the following sets:
 

1. `Lower` case alphabetics
1. `Upper` case alphabetics
1. Digits `0` to `9`
1. `Punctuation marks`/`spacial characters`

### Changing Password For Other User Account

You need to [log in as the root user](https://koompi.org/KOOMPI%20OS#root-info). In order to go into the **root**, type the following command to change the password for User_Name:


```shell
 passwd User_Name
```
or 
```shell
 sudo passwd User_Name
```

**Sample Output:**

```
    [koompi@koompi-pc ~]$ sudo passwd koompi
    New password: 
    Retype new password: 
    passwd: password updated successfully
```
Where, **koompi** – is username or account's name.

> **Noted**: Passwords do not display to the screen when you enter them.
{.is-info}


### Changing Group Password

When the `-g` option is used, the password for the named group is changed. In this example, change the password for the group:

```
    passwd -g Group_Name
```

The current group password is not prompted for. The `-r` option is used with the `-g` option to remove the current password from the named group. This allows group access to all members. The `-R` option is used with the `-g` option to restrict the named group for all users.

### Changing User Passwords On KOOMPI OS

As a KOOMPI OS or Linux system administrator (sysadmin), you can change the password for any users on your server. To change a password on behalf of a user:

1. First sign on or “`su`” or “`sudo`” to the “`root`” account on **KOOMPI OS**, run: `sudo -i`
1. Then type, `passwd Administrator_name` to change a password for Admin user
1. The system will prompt you to enter a password twice

#### Conclusion
The passwd command line utility is used to update or change user’s password. The encrypted password is stored in `/etc/shadow` file and account information is in `/etc/passwd file`. To see all user account try **grep command** or **cat command** as follows:

```
 cat /etc/passwd
 grep '^userNameHere' /etc/passwd
```
The **root** account on a KOOMPI OS computer is the account with full privileges. Root access is often necessary for performing commands in PionuxOS, especially commands that affect system files. Because root is so powerful, it's recommended to only request root access when necessary, as opposed to logging in as the root user. This can help prevent accidental damage to important system files.

# Root Info
### Root Access In Terminal(Konsole)

1. **Open the terminal**. If the terminal is not already open, open it. Many distributions allow you to open it by pressing `Ctrl+Alt+T`.
1. Type **su -** and **press ↵** Enter. This will attempt to log you in as `super user`. You can actually use this command to log in as any user on the machine, but when left blank it will attempt to log in as root.
1. **Enter the root password when prompted**. After typing ***su -** and **press ↵** Enter, you'll be prompted for the root password.
If you get an "authentication error" message, your root account is likely locked. See the next section for instructions on unlocking it.
1. **Check the command prompt**. When you are logged in as root, the command prompt should end with `#` instead of `$`.
1. Now you can use any commands that required root.

### Logout Of Root
You can **Logout of Root** in two ways:
**+ First Way, Type:**

```
exit
```
**+ Second Way,Press:**
```
     CTRL+D
```
### Unlocked The Root Account
1. **Unlock the root account (KOOMPI OS)**. KOOMPI OS locks the root account so that the average user can't access it. This is done because accessing root is rarely necessary when using the `sudo` command (see the previous section). Unlocking the root account will allow you to log in as root.
```
sudo passwd root
```
2.  **Open the terminal**. If the terminal hasn't opened yet. Many distributions allow you to open it by pressing `Ctrl+Alt+T`.
3. Type `sudo passwd root` and `press ↵ Enter`. When prompted for a password, enter your *user* password.
4. `Set a new password`. You'll be prompted to create a new password and enter it twice. Once a password has been set, the root account will be active.
5. `Lock the root account again`. If you want to lock the root account, enter the following commands to remove the password and lock root:
```
 sudo passwd -dl root
```



# Querying Package Database
```shell
    $ pi -Q      #queries the local package database
    $ pi -s      #sync database
    $ pi -F      #files database
```
For more options about querying:
```shell
    $ pi -Q --help
```
Options:
```shell
  -b, --dbpath <path>               # set an alternate database location
  -c, --changelog                   # view the changelog of a package
  -d, --deps                        # list packages installed as dependencies [filter]
  -e, --explicit                    # list packages explicitly installed [filter]
  -g, --groups                      # view all members of a package group
  -i, --info                        # view package information (-ii for backup files)
  -k, --check                       # check that package files exist (-kk for file properties)
  -l, --list                        # list the files owned by the queried package
  -m, --foreign                     # list installed packages not found in sync db(s) [filter]
  -n, --native                      # list installed packages only found in sync db(s) [filter]
  -o, --owns <file>                 # query the package that owns <file>
  -p, --file <package>              # query a package file instead of the database
  -q, --quiet                       # show less information for query and search
  -r, --root <path>                 # set an alternate installation root
  -s, --search <regex>              # search locally-installed packages for matching strings
  -t, --unrequired                  # list packages not (optionally) required by any package (-tt to ignore optdepends) [filter]
  -u, --upgrades                    # list outdated packages [filter]
  -v, --verbose                     # be verbose
      --arch <arch>                 # set an alternate architecture
      --cachedir <dir>              # set an alternate package cache location
      --color <when>                # colorize the output
      --config <path>               # set an alternate configuration file
      --confirm                     # always ask for confirmation
      --debug                       # display debug messages
      --disable-download-timeout    # use relaxed timeouts for download
      --gpgdir <path>               # set an alternate home directory for GnuPG
      --hookdir <dir>               # set an alternate hook location
      --logfile <path>              # set an alternate log file
      --noconfirm                   # do not ask for any confirmation
      --sysroot                     # operate on a mounted guest system (root-only)
```
>  **Warning**: Sometimes, -s's builtin ERE (Extended Regular Expressions) can cause a lot of unwanted results, so it has to be limited to match the package name only; not the description nor any other field.
{.is-warning}
# Searching Packages
**Pi** can also use for the search for packages in the database `(package_name and descriptions)`:
```shell
 pi -Ss String
```
**Example :**
```
pi -Ss '^vim-'
```
To Search for installed package:
```
pi -Qs String1 String2 ...
```
To display extensive information about the given packages:
```
 pi -F String1 String2
```
> **Tips**: Passing two `-i` flags will also display the list of backup files and their modification states.
{.is-success}

```
    $ pi -Qii package_name
```
To verify the presence of the files installed by a package:
```
    $ pi -Qk package_name
```

> **Tips**: Passing the `k` flag twice will perform a more thorough check.
{.is-success}

# Cleaning The Package Caches
**Pi** stores its downloaded packages in `/var/cache/pacman/pkg/` and does not remove the old or uninstalled versions automatically. This has some advantages:

**1. It allows to `downgrade a package` without the need to retrieve the previous version through other means, such as the `Arch Linux Archive.`**
**2. A package that has been uninstalled can easily be reinstalled directly from the cache folder, not requiring a new download from the repository.**

However, it is necessary to `deliberately clean up the cache` periodically to prevent the folder to grow indefinitely in size.

The paccache script, provided within the `pacman-contrib` package, deletes all cached versions of installed and uninstalled packages, except for the most recent 3, by default:
```
paccache -r
```
**Enable and start** `paccache.timer` to discard unused packages weekly.

> **Tips**: You can create a `hook` to run this automatically after every pi transaction.
{.is-success}


For more **options** aboout `paccache` use :
```
 paccache -h
```
**Pacman** also has some built-in options to clean the cache and the leftover database files from repositories which are no longer listed in the configuration file `/etc/pacman.conf`. 

However, *Pacman* does not offer the possibility to keep a number of past versions and is, therefore, more aggressive than paccache default options.

To remove all the `cached packages` that are not currently installed, and the `unused sync database`, execute:
```
 pi -Sc
```

To remove all files from the cache, use the clean switch twice, this is the most aggressive approach and will leave nothing in the cache folder:
```
    pi -Scc
```
> **Warning**: One should avoid deleting from the cache all past versions of installed packages and all uninstalled packages unless one desperately needs to free some disk space. This will prevent downgrading or reinstalling packages without downloading them again.
{.is-warning}

> **Tips:** Automatically clean the package cache.
{.is-success}


If you are too lazy to clean the package cache manually, you can automate this task using Pacman hooks. The Pacman hook will automatically clean the package cache after every Pacman transaction.


To do so, create a file /etc/pacman.d/hooks/clean_package_cache.hook:
```Text
     sudo mkdir /etc/pacman.d/hooks
```
Next:
```Text
    sudo nano /etc/pacman.d/hooks/clean_package_cache.hook
```
Add the following lines:
```Text
    [Trigger]
    Operation = Upgrade
    Operation = Install
    Operation = Remove
    Type = Package
    Target = *
    [Action]
    Description = Cleaning pacman cache...
    When = PostTransaction
    Exec = /usr/bin/paccache -r
```
Save and close the file. From now on, the package cache will be cleaned automatically after every Pacman transactions (like an upgrade, install, remove). You don’t have to run paccache command manually every time.


# Other Operations

**Operations:**

```shell
    $ pi {-h --help}
    $ pi {-V --version}
    $ pi {-D --database}    # <options> <package(s)>
    $ pi {-F --files}       # [options] [package(s)]
    $ pi {-Q --query}       # [options] [package(s)]
    $ pi {-R --remove}      # [options] <package(s)>
    $ pi {-S --sync}        # [options] [package(s)]
    $ pi {-T --deptest}     # [options] [package(s)]
    $ pi {-U --upgrade}     # [options] <file(s)>
```

New operations:

```shell
    $ pi {-Y --pi}          # [options] [package(s)]
    $ pi {-P --show}        # [options]
    $ pi {-G --getpkgbuild} # [package(s)]
```

New options:
```shell 
    --repo                  # Assume targets are from the repositories
    -a --aur                # Assume targets are from the AUR
```

Permanent configuration options:

```shell
    --save                 # Causes the following options to be saved back to the config file when used
    --aururl      <url>    # Set an alternative AUR URL  
    --builddir    <dir>    # Directory used to download and run PKGBUILDS
    --editor      <file>   # Editor to use when editing PKGBUILDs
    --editorflags <flags>  # Pass arguments to editor
    --makepkg     <file>   # makepkg command to use  
    --mflags      <flags>  # Pass arguments to makepkg
    --pacman      <file>   # pacman command to use
    --tar         <file>   # bsdtar command to use
    --git         <file>   # Git command to use  
    --gitflags    <flags>  # Pass arguments to git
    --gpg         <file>   # gpg command to use  
    --gpgflags    <flags>  # Pass arguments to gpg
    --config      <file>   # pacman.conf file to use
    --makepkgconf <file>   # makepkg.conf file to use
    --nomakepkgconf        # Use the default makepkg.conf

    --requestsplitn <n>    # Max amount of packages to query per AUR request
    --completioninterval   # <n> Time in days to to refresh completion cache
    --sortby    <field>    # Sort AUR results by a specific field during search
    --answerclean   <a>    # Set a predetermined answer for the clean build menu
    --answerdiff    <a>    # Set a predetermined answer for the diff menu
    --answeredit    <a>    # Set a predetermined answer for the edit pkgbuild menu
    --answerupgrade <a>    # Set a predetermined answer for the upgrade menu
    --noanswerclean        # Unset the answer for the clean build menu
    --noanswerdiff         # Unset the answer for the edit diff menu
    --noansweredit         # Unset the answer for the edit pkgbuild menu
    --noanswerupgrade      # Unset the answer for the upgrade menu
    --cleanmenu            # Give the option to clean build PKGBUILDS
    --diffmenu             # Give the option to show diffs for build files
    --editmenu             # Give the option to edit/view PKGBUILDS
    --upgrademenu          # Show a detailed list of updates with the option to skip any
    --nocleanmenu          # Don't clean build PKGBUILDS
    --nodiffmenu           # Don't show diffs for build files
    --noeditmenu           # Don't edit/view PKGBUILDS
    --noupgrademenu        # Don't show the upgrade menu
    --askremovemake        # Ask to remove makedepends after install
    --removemake           # Remove makedepends after install
    --noremovemake         # Don't remove makedepends after install

    --cleanafter           # Remove package sources after successful install
    --nocleanafter         # Do not remove package sources after successful build
    --bottomup             # Shows AUR's packages first and then repository's
    --topdown              # Shows repository's packages first and then AUR's

    --devel                # Check development packages during sysupgrade
    --nodevel              # Do not check development packages
    --gitclone             # Use git clone for PKGBUILD retrieval
    --nogitclone           # Never use git clone for PKGBUILD retrieval
    --rebuild              # Always build target packages
    --rebuildall           # Always build all AUR packages
    --norebuild            # Skip package build if in cache and up to date
    --rebuildtree          # Always build all AUR packages even if installed
    --redownload           # Always download pkgbuilds of targets
    --noredownload         # Skip pkgbuild download if in cache and up to date
    --redownloadall        # Always download pkgbuilds of all AUR packages
    --provides             # Look for matching providers when searching for packages
    --noprovides           # Just look for packages by pkgname
    --pgpfetch             # Automatically resolve conflicts using pacman's ask flag
    --nouseask             # Confirm conflicts manually during the install
    --combinedupgrade      # Refresh then perform the repo and AUR upgrade together
    --nocombinedupgrade    # Perform the repo upgrade and AUR upgrade separately

    --sudoloop             # Loop sudo calls in the background to avoid timeout
    --nosudoloop           # Do not loop sudo calls in the background

    --timeupdate           # Check packages' AUR page for changes during sysupgrade
    --notimeupdate         # Do not check packages' AUR page for changes
```

Show specific options:

```shell
    -c --complete         # Used for completions
    -d --defaultconfig    # Print default pi configuration
    -g --currentconfig    # Print current pi configuration
    -s --stats            # Display system package statistics
    -w --news             # Print arch news
```

Pi specific options:

```
    -c --clean            # Remove unneeded dependencies
       --gendb            # Generates development package DB used for updating
```

get pkgbuild specific options:

```
    -f --force            # Force download for existing tar packages
```
*Contributed by @LyhourChhen*

