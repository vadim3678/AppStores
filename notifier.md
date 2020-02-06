# Separating of the application

## The application can be built for different clients: waiter and kitchen.

## Subdirectories

In root directory you can find the folder `bonee-apps` 

```
├───app
├───bonee-apps
│    ├───kitchen
│    │      ├───app
│    │      │   └───App_Resources 
│    │      │       ├───Android  
│    │      │       └───iOS
│    │      └───another-folders           
│    │    
│    └───waiter
│           ├───app
│           │   └───App_Resources 
│           │       ├───Android  
│           │       └───iOS
│           └───another-folders     
```

folders "kitchen" and "waiter" contains subfolder to be changed while compiling

### Scripts

In the `scripts` section of `package.json` add script for new application

```json
    "scripts": {
        "load-waiter-b": "node switcher.js --appPath=waiter && tns build android",
		"load-kitchen-b": "node switcher.js --appPath=kitchen && tns build android"
    }
```
Now you can build the application for example for waiters just running the script

```
npm run load-waiter-b
```

The `switcher.js`, which you can find in the root directory, takes client name from environment variable `appPath`. It changes application id in the `package.json` file

``` json
"nativescript": {
		"id": "net.bonee.waiter",
        
}     
```
 
Another script `prep-bonee.js` located in `hooks/before-prepare/` changes folders and files from main `app/` directory with folders and files from `bonee-apps/kitchen/` or `bonee/apps/waiter` relying on application id in `package.json` when application is building or running.