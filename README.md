Simple reflected light meter
=========================

Simple reflected light meter application for android.

https://play.google.com/store/apps/details?id=com.gmail.mugcuposup.android

How to build
------------

1. Clone repository
<pre>
git clone https://github.com/ayampolsky/SimpleReflectedLightMeter.git
cd ./SimpleReflectedLightMeter/
</pre>
2. Create keystore. Fill in correct certificate details.
<pre>
keytool -genkeypair -v -keystore keystore.jks -alias lightmeter -keyalg RSA \
  -keysize 2048 -validity 10000 -storepass 123456 -keypass 123456 \
  -dname "CN=NAME, O=ORGANIZATIONAL_UNIT, L=LOCATION, C=COUNTRY_CODE"
</pre>
3. Generate APK
<pre>
./gradlew assembleRelease
</pre>
The resulting APK will be `./build/output/apk/release/SimpleLightMeter-1.x.apk`.
