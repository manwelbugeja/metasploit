# Attacking DIVA with Metasploit 3
Injecting the DIVA application is not the only way to attack. An attacker could also inject different apps to acquire a meterpreter. However, the meterpreter would be limited to the injected application's directory; the Android sandbox makes sure it does. With that being said, Android applications can still escape the sandbox, provided the device is rooted. 

An app that requires root privileges must be granted these privileges explicitly from the user on most rooted devices. As such, it would make sense that the injected application is one that already requires these privileges so that the user would not be suspicious of the request. 

The application is injected and installed in the device to start the attack (figures 1 and 2). A meterpreter session is obtained and put in the background, as seen in figure 3. After the application on the device, root permissions are requested. For this test, Magisk was installed on the AVD. 


![alt text](images/3/problem_outline.png)

*Figure  1 - The problem outline.*

## Sources
https://github.com/shakalaca/MagiskOnEmulator

