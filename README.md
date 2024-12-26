## Install

For those curious, the repository is located here: https://git.freepbx.org/projects/FL/repos/freepbx-module-generator/browse

`cd /usr/src wget http://raw.githubusercontent.com/atsip-ru/freepbx-module-generator/master/freepbxgenmod?at=refs%2Fheads%2Fmaster -O freepbxgenerator.phar && chmod +x freepbxgenerator.phar`

This will download the module builder phar and make it executable

## Use

Run the command

`./freepbxgenerator.phar`

Answer the questions

```
Do you want to create a FreePBX or a UCP 14+ module? [Both]
  [0] FreePBX
  [1] UCP 14+
  [2] Both
 > 2
What is your module's name (no spaces)? [helloworld] ariblacklist
What is your module's version? [14.0.1] 15.0.1
What is your module's description? [Generated Module] Blacklist calls with ARI
What is the license for this module? [AGPLv3]
  [0] GPLv2
  [1] GPLv3
  [2] AGPLv3
  [3] MIT
 > 2
What type of module is this? [Connectivity]
  [0] Admin
  [1] Applications
  [2] Connectivity
  [3] Reports
  [4] Settings
 > 1
```

Confirm your information

```
enerate a module with the following information? 
Module type: FreePBX 
Module rawname: ariblacklist 
Module version: 15.0.1 
Module description: Blacklist calls with ARI 
Module type: Applications 
Module License: AGPLv3 Type [yes|no]:yes`
```

The module skeleton will be created

```
Generating Directories for your module 
Generating File structure for your module 
Generating module.xml 
Generating BMO class 
Generating module page and view 
Generating UCP Module class 
Generating UCP Module Global JS 
Generating UCP Module Less file 
Linking your module folder into the framework module folder 
<snip> 
Module ariblacklist successfully installed    

Updating Hooks... 
Done

Reloading 
Reloading FreePBX    

Successfully reloaded
```

The module has been fully installed into freepbx and is ready for development

You can cd to the module in the above case ariblacklist and the following structure will be in place

```
[root@system ariblacklist]# tree
.
├── Ariblacklist.class.php
├── assets
│   ├── css
│   │   └── ariblacklist.css
│   └── js
│       └── ariblacklist.js
├── install.php
├── LICENSE
├── module.xml
├── page.ariblacklist.php
├── README.md
├── ucp
│   ├── Ariblacklist.class.php
│   ├── assets
│   │   ├── js
│   │   │   └── global.js
│   │   └── less
│   │       └── Ariblacklist.less
│   └── views
│       ├── ariblacklist.php
│       ├── user_settings.php
│       └── willy.php
├── uninstall.php
└── views
    ├── main.php
    └── ucp_config.php
```

## What's Next?

After you've setup your module you're probably asking yourself, "Okay, what now?". The best next step would be starting with [FreePBX Development](https://wiki-legacy.freepbx.org/display/FOP/FreePBX+Development) to get a general overview of functions and methods from within FreePBX

Another great place to start is by looking over the [FreePBX Internals](https://wiki-legacy.freepbx.org/display/FOP/FreePBX+Internals) wiki pages. These pages should help give you a brief overview of FreePBX and deep dive into specific functions and methods    
