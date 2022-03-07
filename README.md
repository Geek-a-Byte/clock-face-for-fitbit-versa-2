# clock-face-for-fitbit-versa-2

## ``Step 1 : Connect your smartwatch and mobile with fitbit studio``

- go to account from android app, click on versa 2 from synced devices **make sure you have set up your wifi on your versa beforehand**
- go to developer menu and push the connect button
- go to the fitbit simulator and select your phone from 'select your simulator section'
- don't forget to turn on developer bridge from your versa 2 settings, you need to wait for a while to pair up your phone app with your versa 2

at last you may see the following results in your simulator console

![image](https://user-images.githubusercontent.com/59027621/156912571-a7877aa1-8f41-4476-b1ff-637292a75c1f.png)

## ``step 2``

```console
npx create-fitbit-app <project-name>
cd <project-name>
```

## ``step 3: change in package.json file``

- sdk version to 4.1.0
- build targets to "mira" only

## ``step 4: change the index.view to index.gui and widgest.defs to widgets.gui``

## ``step 5``

```console
npm install
npx fitbit-build
npx fitbit
fitbit$ install
fitbit$ bi
```

- now login with your creds
- follow this [now](https://dev.fitbit.com/getting-started/)



## ``Issues``

### ``problem 1 : if you had continued with fitbit studio instead of cli``

![image](https://user-images.githubusercontent.com/59027621/156912706-f976c44d-944d-45f6-a9ba-634220829a14.png)

- [``solution``](https://community.fitbit.com/t5/SDK-Development/SDK-4-2-broken/m-p/4620720#M13877)

![image](https://user-images.githubusercontent.com/59027621/156912722-ead6729d-9477-43af-befe-524d41684cf4.png)

### ``problem 2 : if you had continued with fitbit studio instead of cli``
 
![image](https://user-images.githubusercontent.com/59027621/156912890-66aaad17-a29e-416a-92db-42cf4b10183c.png)

- solution - this is where the main problem started.. :facepalm: I need to shift to CLI mode for development 
- [explanation](https://community.fitbit.com/t5/SDK-Development/Sideload-of-app-failed-Connected-device-does-not-support-API-version/td-p/4584270) : my fitbit versa 2 has an in built sdk version of 4.1 which is not compatible with 4.3 which I started the project with in fitbit studio. and sigh there is no option for degrading the sdk version in fitbit studio so I have to go for cli mode to build the clock face.

### ``problem 3 : you need nodejs version 14.19.0 to work with the commands of fitbit cli guide``

- started following the cli guide - https://dev.fitbit.com/build/guides/command-line-interface, where they forgot to mention that you need node js version 14.19.0 to be installed as prerequisite which costed me at least 10 hours of test and trials of web solutions, thanks to a complete stranger at discord group discussion :grateful:
- you'll need chocolatey to download nodejs specific version for windows
- https://community.chocolatey.org/packages/nodejs/14.19.0
- I'll remember this - 
![image](https://user-images.githubusercontent.com/59027621/156930172-386bad6c-9a54-42d1-9581-4bdab11a1f61.png)
