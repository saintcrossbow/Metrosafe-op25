# op25 Metrosafe Data

Details and setup for Louisville Metrosafe with op25.

**Method**

The basic creation of op25 is fully documented: https://www.hagensieker.com/wordpress/2018/07/17/op25-for-dummies/

The difficult and tedious work is assembling the frequencies, and that is the work this repo provides.

1. Use the hagensieker setup method
2. Replace the trunk.tsv file with the one in this repo
3. Add metrosafe.tsv

**Additional notes**
* When you start the program, you may have to nudge the frequency left (, key) or right (. key). Every time I start it, I move to the right twice.
* A sample script that starts op25 without listening to encrypted files:

```
#!/bin/sh
echo Starting op25 with crypt filtering...
# TODO: Your starting directory will likely vary
cd ~/Tools/op25/op25/gr-op25_repeater/apps
./rx.py --args 'rtl' -N 'LNA:47' -S 2400000 -f 854.4875e6 -n -o 25000 -q -1 -T trunk.tsv -V -2 -U 2> stderr.2
gain: name: LNA range: start 0 stop 0 step 0
```

*This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.*

*This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.See the
GNU General Public License for more details.*

*You should have received a copy of the GNU General Public License
along with this program.If not, see http://www.gnu.org/licenses/*

