# android-signer

Using JDK 8

if you not have JDK 8, you can download in here https://github.com/frekele/oracle-java/releases

`USAGE :`

`/bin/java -jar sign.jar [name].apk`

# Manuall signer with zipalign and apksigner

```
zipalign -f -v 4 release.RE.apk release.RE.zipalign.apk

apksigner sign -v --out release.RE.saved.apk --ks ~/Tools/android-signer/my-release-key.keystore --ks-key-alias alias release.RE.zipalign.apk
```

# Other way
```
zipalign -p -f 4 release.RE.apk release.RE.zipalign.apk
```
