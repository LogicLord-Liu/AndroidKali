# HELLO EVERYONE
This passage will show you how to install Kali Linux in Android.

* Requirements
  >A Physical Android Phone. You can do this install on an Android 12+ phone, I will show 
  >you how to mitigate the problems with Android 12+ Phantom Processes. See the link to 
  >the article below on GitHub on how Android monitors and kills forked child processes 
  >of apps when they use too much of the CPU.https://github.com/termux/termux-app/issues/2366
* Android Kali NetHunter Rootless Install.
  >1.You will need to install Termux. You can get Termux from the F-Droid store or from their 
  >GitHub repo using one of the following links (In the demo we use GitHub):
  >* https://f-droid.org/packages/com.termux/
  >* https://github.com/termux/termux-app/releases
  >
  >Take note that the official Termux Wiki and Termux GitHub pages indicates that you 
  >should not install the outdated version hosted on the Google Play Store.
  >
  >2.Download the latest Termux version at the time of writing it is termux-
  >app_v0.118.0+github-debug_arm64-v8a.apk from the github link above.
  >
  >3.Open and Install the downloaded Termux APK file.Press on Install and then Open.
  >
  >![Termux](https://img-blog.csdnimg.cn/db4d94074b874a7090ca0f5c5a716678.png)
  >
  >![File](https://img-blog.csdnimg.cn/6265f5b0bdc843239dac551554b48e07.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6YaJ44CB5YC-5Z-O,size_20,color_FFFFFF,t_70,g_se,x_16)
  >
  >4.Enter the following command: `Pkg Update -y`
  >
  >5.When prompted for an action press **Y** and <**Enter**> so you install the package 
  >maintainer’s version.
  >
  >6.Enter the following commanded: `termux-setup-storage`
  >>In order to have shared storage you need to give Termux storage access permission.
  >>
  >>**Don't give access to external connected storage devices.**
  >>
  >>7.Install wget and when you’re asked Do you want to continue, press Y and Enter.
  >>`pkg install wget`
  >>
  >>8.When you get asked to "Do you want to continue " press **Y** and **Enter**
  >>
  >>9.Download the NetHunter install file. **Enter that you enter the correct adress.**
  >>
  >>`wget -O install-nethunter-termux https://offs.ec/2MceZWr`
  >>
  >>10.Change the permissions so that you can execute the file:`chmod +x install-nethunter-termux`
  >>
  >>11.Type the following command to execute the downloaded install file:`./install-nethunter-termux`
  >>
  >>12.Enter the image that you want to install. We are going to install **1**.
  >>
  >>13.The installation will take a while, when asked to delete rootfs, enter **N**.
  >>
  >>14.To start Kali NetHunter you can use the following commands:
  >>* To start the CLI `nethunter`
  >>* To setup the NetHunter KeX password `nethunter kex passwd`
  >>* To start NetHunter KeX (Password will ve set on first startup) `nethunter kex`
  >>* To stop the NetHunter KeX GUI `nethunter kex stop`
  >>* To run NetHunter as root `nethunter -r`
  >>* You replace nethunter with nh in all these commands. `nh`

* Android Kali NetHunter Rootless Install-Fix dbus-x11 error
  >1.To fix the dbus-x11 error, run nh -r
  >
  >2.Open the file/etc/resolv.conf with nano.
  >
  >3.Edit the ip address to be 8.8.8.8
  >
  >4.Press ctrl + x and enter **Y** to save the file.
  >
  >5.Run apt update.
  >
  >6.Run apt install dbus-x11 -y
  >
* Android Kali NetHunter Rootless Install-Stop killing of child processes.
  >1.Unlock Developer options.
  >
  >![Developer](https://img-blog.csdnimg.cn/img_convert/51d528795350a9e3b4f2c3529fdb5866.png)
  >
  >![Developer](https://img-blog.csdnimg.cn/img_convert/e4e38d989a73336fccc779ae467190e6.png)
  >
  >![Developer](https://img-blog.csdnimg.cn/img_convert/2d19b9ebb2af8a8bf654265603ede0f0.png)
  >
  >2.Go to Developer options and ensure Disable child process restrictions is turned on.
  >
* Android Kali NetHunter Rootless Install-Start nh and nh kex
  >1.Once you run nh you are now in the Kali NrtHunter CLI.
  >
  >2.You can exit the NrtHunter CLI by entering **exit**.
  >
  >3.Set the password for KeX VNC by running nh kex for the first time. You’ll use the password.
  >
* Android Kali NetHunter Rootless Install.
  >4.Remember the port number. You will use it in Step 29.
  >
  >5.Set the password for KeX VNC by running nh kex for the first time. Say no to entering a 
  >view-only password.
  >
  >6.Go to the Kali NetHunter APP Store website: https://store.nethunter.com/en/
  >
  >7.Download the NetHunter APP Store.
  >
  >8.Press on the Hamburger button of your browser,go to downloads and install NetHunterStore.apk
  >
  >9.Press on the search button and enter KeX.Press to dowmload NetHunter KeX.
  >
  >10.Press on the search button and enter KeX.Press to dowmload and install KeX.
  >
  >![NrtHunter KeX](https://img-blog.csdnimg.cn/img_convert/068706ce51cc0b54c893228333e7d1f0.jpeg)
  >
  >11.You will get a popup window. You click on Settings, and then toggle Allow from this 
  >source. Then press Install.
  >
  >12.Press on Allow to allow NetHunter KeX access to your files on the device.
  >
  >13.Enter the port number from step 20,username as kali,and your password from step 19.Press on Connect.
  >
  >14.You now should have Rootless NetHunter GUI on your Android phone!
  >
  >![Kali Linux](https://img-blog.csdnimg.cn/direct/b9b562e4e7364c91b79698b27d1904d4.jpeg)

#### Now， all of our steps have been completed, and you can proceed with various operations on your phone.
