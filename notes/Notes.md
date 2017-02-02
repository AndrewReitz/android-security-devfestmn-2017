# Let's Talk Security Notes

**Slide 0**: Title
Talk About: Idea for talk

**Slide 1**: Overview
Talk About: What we will cover

**Slide 2-5**: Who am I
Talk about: Pretty Self Explanatory

**Slide 6**: OS Security / Linux
Talk about: Linux Security

Notes from source.android.com
As the base for a mobile computing environment, the Linux kernel provides Android with several key security features, including:

* A user-based permissions model
* Process isolation
* Extensible mechanism for secure IPC
* The ability to remove unnecessary and potentially insecure parts of the kernel
As a multiuser operating system, a fundamental security objective of the Linux kernel is to isolate user resources from one another. The Linux security philosophy is to protect user resources from one another. Thus, Linux:

* Prevents user A from reading user B's files
* Ensures that user A does not exhaust user B's memory
* Ensures that user A does not exhaust user B's CPU resources
* Ensures that user A does not exhaust user B's devices (e.g. telephony, GPS, Bluetooth)


**Slide 7-8**: Application Sandbox

**Slides 9**: Google Extras

The Android Compatibility Device Definition - docs no how android should act
Compatibility Test Suite - suite to ensure devices behave correctly

* Google Play: Google Play is a collection of services that allow users to discover, install, and purchase applications from their Android device or the web. Google Play makes it easy for developers to reach Android users and potential customers. Google Play also provides community review, application license verification, application security scanning, and other security services.
* Android updates: The Android update service delivers new capabilities and security updates to selected Android devices, including updates through the web or over the air (OTA).
* Application services: Frameworks that allow Android applications to use cloud capabilities such as (backing up) application data and settings and cloud-to-device messaging (C2DM) for push messaging.
* Verify Apps: Warn or automatically block the installation of harmful applications, and continually scan applications on the device, warning about or removing harmful apps.
* SafetyNet: A privacy preserving intrusion detection system to assist Google tracking and mitigating known security threats in addition to identifying new security threats.
* SafetyNet Attestation: Third-party API to determine whether the device is CTS compatible. Attestation can also assist identify the Android app communicating with the app server.
* Android Device Manager: A web app and Android app to locate lost or stolen device.

**Slide 10**: Application Security

**Slide 11**: Networking

We could spend a lot of time on this. If you want to learn a lot more
check out Jesse Wilsons talk "HTTP In A Hostile World"

**Slide 12**: Use https

ALWAYS!

**Slide 13**: Cert Pinning

* Explain how certs work
* Go over pros
* Cons

**Slide 14**: Careful with data

Nuff said

**Slide 15**: Storage Security

SQL, Flat Files, and Shared Prefs are all stored in a location that is readable
only to the application. Generally although shared prefs can be setup to be world
readable, but don't do that. Root users can get access to all of these, but
what are they trying to steal there own data?

SD card, anyone, and everyone can read from here, you could encrypt the data
and store the key somewhere internal.

Storing Credentials

**Slide 16**: Apk Issues

Common issues in APKs

**Slide 17**: Recompile / De-compiling

easy to do
you could obfuscate, but that only goes so far

**Slide 18**: Key, Secrets and Passwords

Obfuscation:
- byte arrays and funny names
- ProGaurd
- DexGaurd

Store User Info in account manager

Only real way to store things is to have a user type in a password

**Slide 19**: APIs

Android N, made it more difficult

Cert pinning

Obfusction:
- ProGaurd, DexGaurd
- By Hand Tricky stuff
- HMAC

Build your apis as if they are public

**Slide 20**: Rooting

- Easy to do, and buy passes all sandbox, basically god mode
- You can disallow users from using your app if rooted, unsure of what this accomplishes.
- Use the screen lock
- Use super SU or some other measure of protection, disallows apps and command line access

**Slide 21**: Conclusion

**Slide 22**: Questions
