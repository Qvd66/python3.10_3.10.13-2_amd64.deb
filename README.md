Works! Installed Python 3.10.13 on my emulator with architecture x86_64 which u can get to know in termux by using command uname -m

+++++INSTALLATION+++++ Edited from : https://stackoverflow.com/questions/64853742/need-to-run-python-3-8-x-on-termux-on-android-currently-installed-with-python-3 

Here is a summary of the solution given by @kcubeterm on Reddit, who has very kindly provided a way to install python 3.8X on Termux.


1)Remove python 3.9 if you have it installed:

pkg uninstall python

2) Make a note of the architecture of your device's CPU using this command:

uname -m

3) Download the raw .deb file in termux using web-get as shown below

[4] make sure you add ?raw=true to the end of the url, or else you'll end up downloading the html file!


wget https://github.com/Qvd66/python3.10_3.10.13-2_amd64.deb/blob/main/x86_64%20python3.10_3.10.13-2_amd64.deb?raw=true

5) Finally, execute the following command in termux:
   
   dpkg -i ./'python_3.8.6_x86_64.deb?raw=true'


Hope this answer helped you to install Python 3.10 I love termux but find it frustrating that they provide no way to install non-bleeding edge versions of packages!
                          
Thanks again to @kcubeterm & Joy Boyle who provided this solution.

