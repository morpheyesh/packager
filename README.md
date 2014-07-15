packaging
=========

This project helps in packaging megam - private datacenter.

This has rake files that auto-generates builds for Megam.

In the first phase we plan to provide `deb` support for

***

The list of packages built and their dependency are shown below.

* precise (12.04)
[Precise](images/precise.png)

* trusty (14.04)
[Trusty](images/trusty.png)

How can you build it
-----------------------
Every flavor (ubuntu) has a config.rb and a the version is set in the global version.rb.

Go into one of the directories and

```
cd megamnilavu

#builds a package for trusty
rake

builds a package for precise
rake precise

```



Install  packages
------------------------

* deb

```
sudo add-apt-repository "deb http://get.megam.co/ $(lsb_release -sc) testing"


wget -qO - http://get.megam.co/?? | sudo apt-key add -


sudo apt-get update

sudo apt-get install megamnilavu

sudo apt-get install megamgateway

sudo apt-get install megamanalytics


```

Testing packages
------------------------




#### TO - DO

* build.rb  : A thor file that provides ability to build all the packages in a single comamnd.

```
thor build:clean

thor build:all

thor build:trusty

thor build:precise

```

* deploy.rb : A thor file that deploys the build packages in a server.

```
thor depoly:push

```

# License

|                      |                                          |
|:---------------------|:-----------------------------------------|
| **Author:**          | Yeshwanth (<getyesh@megam.co.in>)
|		       	           | Thomas Alrin (<alrin@megam.co.in>)
| **Copyright:**       | Copyright (c) 2013-2014 Megam Systems.
| **License:**         | Apache License, Version 2.0

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
