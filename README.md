One-to-One Video Call using React Native and Airtel IQ  

This client application in React Native demonstrates how you can implement video calling capabilities in your mobile applications using Airtel IQ Toolkit. The application runs on a device with React Native Framework and utilizes Airtel IQ React Native SDK to conduct an RTC session. The sequential tasks performed by the client application to conduct an RTC session are as given below:  

Fetch token from the application server. 

Connect to the room using the received token. 

Publish media streams in the room. 

Subscribe to remote media streams in the room. 

Observe and handle session-related events. 

The sample application demonstrates the following advance features along with basic video call: 

Mute/Unmute video 

Mute/Unmute audio 

Switch Camera (front or rear) 

Switch to Speaker 

Disconnect 

 

1. Getting Started 

1.1 Pre-Requisites 

 
1.1.1 Authorization Credentials 

Follow the steps given below to generate API Credentials required to access Airtel IQ: 

Create a free account on Airtel IQ 

Create your Project 

Get the App ID and App Key generated against the Project. 

 

1.1.2. Requirements 

A Device to test the sample application as a simulator/emulator does not support playing video or publishing a local Stream. 

Install/update Xcode - 10.0 or higher 

Install/update Android Studio – 6.0 or higher 

 

1.1.3.  Download Sample React Native client  

Clone or download this Repository: https://github.com/Airtel IQ/One-to-One-Video-Calling-Open-Source-React-Native-Application 

 

1.1.4. Configure Sample React Native Client 

Open the App. 

Go to EnxJoinScreen.js and make the following changes: 

/* To try the app with Airtel IQ hosted service you need to set the kTry = true */  

var kTry = true;  

/*Your webservice host URL. Use Airtel IQ host as given below when kTry = true */  

var kBasedURL = "https://demo.Airtel IQ.io/";  

/*The following information is required only when kTry = true. Remove these fields if using your own web-service.*/  

/*Use Airtel IQ portal to create your app and get the following credentials*/ var kAppId = "AppId";  

var kAppkey = "AppKey";  

``  
 

Note: The distributable comes with demo username and password. 

 
1.1.5. Sample application server 

Once you have downloaded the client code, you need to download the server code to provision video room on Airtel IQ server. Use any of the Repositories listed below to setup your application server: 

Laravel 

PHP 

Nodejs 

Python 

C# 

Clone or download a repository of your choice and configure the server as per the instructions given in the respective README document.  

To directly try the sample code without having to configure an application server, you can also use the Airtel IQ test server as explained in section 2. However, it is recommended to configure your own application server to build a video calling application. 

 

1.2. Test 

Open the App in your device.  

A Form to enter the Name and Room ID opens. 

Create a Room by clicking on “Create Room” button. 

Use the Room ID to enter the Room as a Moderator or a Participant and share the Room ID with others who want to join the RTC session in the Room. 

You are now in a video call with others, who have joined the same room. 

Note: This sample application creates a virtual room with limited Participants and 1 Moderator for demonstration purposes. 

 

2. Pre-configured Test Server 

As mentioned in section 1.1.5 above, you have an option to run your client application on Airtel IQ pre-configured environment instead of setting up your own application server.  

This allows you to quickly test the performance of Airtel IQ video calls before getting into the development of your application.  

As the Airtel IQ test server has been configured for demonstration purpose only, it only allows to: 

Conduct a single session with a duration lesser than 10 minutes. 

Host a multiparty call with less than 3 participants. 

Refer to the Demo App Server for more information.   

Once you have successfully tested your application on the test server, you can set up your application server as explained in section 1.1.5 above. 

 

3. Know more about Client API 

The client APIs are called from the Airtel IQ React Native SDK (enx_rtc_react_native) which runs in the client application. The client APIs are used to communicate with the Airtel IQ video services and monitor the client-side state of the RTC session.  

The client APIs are typically used to: 

Connect to the desired room using the token received from the application server 

Manage local audio and video 

Handle room and stream related events initiated by the user 

The client APIs handle four major entities: 

Airtel IQ Room: It handles room/session related events like connection, local stream publication, and remote stream subscription. 

Airtel IQ Stream: It identifies audio/video/data stream published by the user. 

Events: It represents the events related to the room and the stream. 

Player: It represents the customizable UI element used to render the audio/video stream in the DOM. 

In addition to the features demonstrated in this sample program, the SDK has many helpful APIs available for the developers to utilize like: 

Text chat 

Session recording  

File sharing 

Screen sharing 

Annotation 

Streaming 

Canvas 

And many more such exciting features. 

Read React Native Toolkit Documentation for more details. 

Learn how to Install enx_rtc_react_native here 

Note: 

If you are using an older version of react-native (0.60.5) or if you come across the following error: 

Native Module EnxRoomManager tried to override EnxRoomManager. Check the getPackages() method in MainApplication.java. 

Follow the steps given below after executing npm install:   

Go to the enx-rtc-react-native folder in your app 

Find nodemodules folder and delete it 

Sync up your project files. 

 

4. Support 

Airtel IQ provides a library of Documentations, How-to Guides, and Sample Codes to help software developers, interested in embedding RTC in their applications. 

Refer to the Complete Developer’s Guide for more details. 

You may also write to us for additional support at support@Airtel IQ.io. 

 