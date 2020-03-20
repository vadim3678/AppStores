# Process of adding new application into apple store 

### Creating app identifier
 go to 
```
https://developer.apple.com/account/resources/identifiers/list
```
then create identifier

![Adding identifier](https://github.com/vadim3678/AppStores/blob/master/images/ios/1.jpg)

select app options and fill bundle id

![Registering features](https://github.com/vadim3678/AppStores/blob/master/images/ios/2.jpg)

> for some options you will need to add a certificate

### Creating an app

Go to apple app store connect -> My Apps and select app type you want to add

![Adding an app](https://github.com/vadim3678/AppStores/blob/master/images/ios/3.jpg)

... fill form using identifier you have created

![Adding an app](https://github.com/vadim3678/AppStores/blob/master/images/ios/4.png)

### Adding certificates

For some option you need to add certificates. You have to find keychain app on Mac and create cerificate request

![Creating request](https://github.com/vadim3678/AppStores/blob/master/images/ios/cert_3.png)

Fill email, request name and save it to disk 

![Saving request](https://github.com/vadim3678/AppStores/blob/master/images/ios/cert_4.png)

Request file on disk

![Request in finder](https://github.com/vadim3678/AppStores/blob/master/images/ios/cert_5.png)

Then return to apple connect console where you have created app identifier and start adding certificate

![Adding certificate](https://github.com/vadim3678/AppStores/blob/master/images/ios/cert_1.png)

You will be redirected to loading request page. Upload request you have created on Mac

![Loading request](https://github.com/vadim3678/AppStores/blob/master/images/ios/cert_2.png)

Download certificate to Mac

![Downloading certificate](https://github.com/vadim3678/AppStores/blob/master/images/ios/cert_6.png)

Find created certificate and execute it. After that it will appear on Keychain app

![Certificate in keychain](https://github.com/vadim3678/AppStores/blob/master/images/ios/cert_7.png)

