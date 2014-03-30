# xcodefly
Speeds up Xcode builds by moving the DerivedData folder to a RAM disk. Original idea by [Steve Madsen](https://lightyearsoftware.com/2012/08/use-a-ram-disk-for-deriveddata).

## Install

```
sudo curl -o /usr/local/bin/xcodefly https://raw.githubusercontent.com/soheilpro/xcodefly/master/xcodefly && sudo chmod +x /usr/local/bin/xcodefly
```

## Usage

```
xcodefly start [size]
```
Creates a RAM disk with the specified size and mounts it at ~/Library/Developer/Xcode/DerivedData.
- size: size of the RAM disk, in 512 byte sectors. Default is 4194304 (a 2 GB volume)

```
xcodefly stop
```
Unmounts the RAM disk.

```
xcodefly install [size]
```
Creates a Launch Agent to run the script at startup.
- size: size of the RAM disk, in 512 byte sectors. Default is 4194304 (a 2 GB volume)

```
xcodefly uninstall
```
Removes the Launch Agent.

## Version History
+ **1.0**
	+ Initial release.

## Author
**Soheil Rashidi**

+ http://soheilrashidi.com
+ http://twitter.com/soheilpro
+ http://github.com/soheilpro

## Copyright and License
Copyright 2014 Soheil Rashidi

Licensed under the The MIT License (the "License");
you may not use this work except in compliance with the License.
You may obtain a copy of the License in the LICENSE file, or at:

http://www.opensource.org/licenses/mit-license.php

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
