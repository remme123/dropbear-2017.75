## build
```shell
./configure --disable-syslog --host=aarch64-linux-android --disable-zlib CFLAGS='-D__ANDROID_API__=22 -fPIE' LDFLAGS='-fPIE -pie'
make -j && make -j scp
tar cf db.tar dbclient dropbear dropbearkey dropbearconvert scp
adb push db.tar /sdcard/
```
