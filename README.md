# About
This is a **rtlwifi driver**.When your Linux OS prompt **Error** message such as "**No Wifi Adapter Found**",in Wifi tab.</br>
So here I am with the solution to resolve this issue.

## How to Install?
### Steps:
1.Download the attached **rtlwifi_new.tar.gz** folder and extact it in path **/home/*user_name*.**</br>
2.Open Terminal and Run the following commands one by one.</br>
&nbsp;&nbsp;&nbsp;$ cd rtlwifi_new</br>
&nbsp;&nbsp;&nbsp;$ make all</br>
&nbsp;&nbsp;&nbsp;$ sudo make install</br>
&nbsp;&nbsp;&nbsp;$ make clean</br>
3.Reboot the system</br></br>
*Now your **wifi will start working.*** :+1: </br></br>
*Still if not working,then Open Terminal & Run the command* **$ crontab -e**</br>
Now,</br>
1.Select the *Nano-Editor*</br>
2.Press **ctrl + O** & the paste the following line in the editor</br>
&nbsp;&nbsp;&nbsp;&nbsp;@reboot /bin/sh /home/user_name/rtlwifi_new/abc.sh</br>
3.Press **ctrl + X**</br>
4. Open Terminal & Run the following commands:</br>
&nbsp;&nbsp;&nbsp;$ cd /home/prashant_singh/rtlwifi_new</br>
&nbsp;&nbsp;&nbsp;$ gedit abc.sh</br>
5.Paste the following line in the editor</br>
&nbsp;&nbsp;&nbsp;&nbsp;sudo modprobe -r rtl8723de  && sleep 5 && sudo modprobe rtl8723de ant_sel=2,</br></br>
Hope this Helps :+1:
