**Splash** screen is a screen that loads when you launch an app. When you first open your application, a loading screen, also known as a launch screen or startup screen, appears. You’ll be brought to a more useful screen where you can perform activities after the loading is complete.

Splash screens only appear briefly on your screen; if you turn your head away, you can miss them. Typically, you’ll notice the company name, emblem, and, with any luck, the company motto.
<img width="511" alt="img11" src="https://github.com/tanujav988/Android-Learning/assets/73555975/73ded3c5-3fab-45f4-9042-35d3d9d611cf">

Step1 : Create 2 Files 

1. XML file
2. Java file



Step2 : Design : Image View and TextView in Relative Layout

<img width="427" alt="img12" src="https://github.com/tanujav988/Android-Learning/assets/73555975/e5ef73b3-3eb1-494d-947a-8a35888974bb">

<br>
<br>
Step3 : Java Code <br>
<br>
<img width="1440" alt="img13" src="https://github.com/tanujav988/Android-Learning/assets/73555975/f642732f-85c3-445b-9a45-2a7b4ee15dbb">

```
        Thread thread = new Thread(){
            public void run(){
                try{
                    sleep(4000);
                }catch(Exception e){
                    e.printStackTrace();
                }
                finally {

                    Intent intent = new Intent(SplashActivity.this, MainActivity.class);
                    startActivity(intent);
                }
            }
        };thread.start();
```


<br>
<br>
Step4 : Modifying AndroidManifest.xml
<br> <br>
<img width="1440" alt="img14" src="https://github.com/tanujav988/Android-Learning/assets/73555975/e1feb70e-d148-494f-9c8c-deecc299a452">

```
 <intent-filter>
            <action android:name="android.intent.action.MAIN" />

            <category android:name="android.intent.category.LAUNCHER" />
        </intent-filter>
```


Adding the intent filter part to the SplashActivity as it was by default present with the MainActivity
