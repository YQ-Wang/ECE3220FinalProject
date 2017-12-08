# ECE3220 Final Project

## Video URL
https://www.youtube.com/watch?v=xSwDqnKpt9g

## Team Member
* Chunbin Lin (clpk8)
* Yiqing Wang (yw283)

## How to install?
Running our system on Mac is simple. The IDE you need to install is Qt. Following are the steps to install our system.

### Steps
* Install Qt IDE: https://www1.qt.io/download-open-source/?hsCtaTracking=f977210e-de67-475f-a32b-65cec207fd03%7Cd62710cd-e1db-46aa-8d4d-2f1c1ffdacea
* Clone our project to your local repository by using 
```sh
git clone https://github.com/clpk8/ECE3220FinalProject.git
```
* Open up the folder **Mizzou Checkout v2**. Right click on **Mizzou Checkout**, select **Show Package Contains**.
* Open **Contents** folder inside it, then open **MacOs** folder. 
* Launch **Mizzou Checkout** executable file, then the program will start running. 
* In order to input a new record of ID to the database, open the terminal and open the directory to MacOs, and type the following commands to insert the new ID into table User.
```sh
sqlite3 <the directory to MacOS>/FP.db;
INSERT INTO User (StudentId) VALUES (your id);
```
* The pawprint and password for are **admin1** & **HelloWorld**.

## If you want to run our system on other systems you need to compile it.
* In order to compile our application on your local machine, you need to have Qt, OpenCV library and Zbar library installed. But our SendMail functionality is design for MacOS only.
* http://rodrigoberriel.com/2014/10/installing-opencv-3-0-0-on-ubuntu-14-04/ 
  Above url provides you with a step by step guide on installing OpenCV on Ubuntu. On Mac and other Linux systems you can also just do Brew install OpenCV in the terminal. 
* Installing Zbar in Mac and Linux is simple as well. Brew install Zbar in the terminal will solve the issue. 
* https://www.learnopencv.com/configuring-qt-for-opencv-on-osx/ 
  Now you need to configure OpenCV and Zbar to the Qt. Link below will give you a step by step guide on configuring it to the Qt using pkg-config and a tutorial video. The video only show you how to link OpenCV, but how to link Zbar is similar. Follow the step they done with opencv, and replace with zbar in this time.
* After you have done those, all you need to do is open the **ECE3220FinalProject.pro** file inside the **ECE3220FinalProject** folder, and run Qmake on the Qt (located on top left corner inside the build), now you are able to compile the application and run it.
