# networking_and_preferences

## Note

We're using http to call Movie DB end points in this example. https is more secure for sure, however, we used http to make it simpler for you to run this app on older devices. The case is as the following: 

https uses SSL or TLS to be secured, Android versions that are less than 4.4 support certain versions of SSL and TLS, while Android versions greater than 4.4 support certain versions of SSL and TLS.  

This can cause an error if the version supported by the used Android device is different from the one used at the server endpoint. So, you'll need to add some code to your app to support a specific version of the protocol that can work with the server. When you add that code, the app will use the protocol version you specified in the code regardless of Android OS version, and this enables your app to run on old and new devices. 

Here are some resources (you can search further in other resources):
https://stackoverflow.com/questions/36888852/javax-net-ssl-sslexception-connection-closed-by-peer-on-4-4-2-device-works-on
https://stackoverflow.com/questions/48895516/javax-net-ssl-sslexception-connection-closed-by-peer-on-volley-android-4-4

So if your min SDK supports devices with Android version less than 4.4 and you want to use https (or the server only supports https) you'll need to add that extra code, otherwise if it supports devices with version greater than 4.4 you can use https without any additional code. 
