# This repo contains three modules. 
+ `fdll`  a shared library, libfdll.so, implements functions declared in `include/aug.h`
+ `sdll`  a shared library, libsdll.so, implements functions declared in `include/aug.h`
+ `app`   an executable program, linked `libsdll.so`. 

# Output
When executing ./app/app, lines shown in terminal likes:
```
[root@test-server cpp]# ./app/app
1 + 2 = -4
```
When `libsdll.so` is replaced by `libfdll.so` with shell command `mv fdll/libfdll.so sdll/libsdll.so`, the output of `app` is not the same as before:
```
[root@test-server cpp]# mv fdll/libfdll.so sdll/libsdll.so
mv: overwrite ‘sdll/libsdll.so’? y
[root@test-server cpp]# ./app/app
1 + 2 = 3
[root@test-server cpp]#
```


# How to build
```
$ cmake . 
$ make 
```
