# inc4is_pg16_libraries
 postgresql 16.3 libraries copy for doing code analysis
 (h) librares for intellisense 

 All *.h files are copied from Rocky Linux 8 that runs pg16.3.
 for just analysis/read the codes not for applicable to build or debug or any kind of..
 the files are required for postgresql-16 code analysis.

 You should install mysy2 & mingw & gpp etc

 https://code.visualstudio.com/docs/cpp/config-mingw

 msys & mingw releated dirs are located on c:\swdepot dir
 After mysy2 & mingw setups are finished complete with below steps

```bash
$ cd /c/swdepot

$ wget https://ftp.postgresql.org/pub/source/v16.3/postgresql-16.3.tar.gz

$ tar -xf postgresql-16.3.tar.gz
```
```console
mkdir c:\swdepot
cd c:\swdepot
git clone 
```
## My c_cpp_properties.json file for intellisense "*.h file not found" crap (if you wish) to overwrite it

```json

{
    "configurations": [
        {
            "name": "gcc msys",
            "includePath": [
                "${workspaceFolder}/**",
                "C:\\swdepot\\inc4is_pg16_libraries\\*",
                "C:\\swdepot\\msys64\\usr\\include\\**",
				"C:\\swdepot\\msys64\\mingw64\\include\\**",
				"C:\\swdepot\\postgresql-16.3\\**",
                "C:\\swdepot\\postgresql-16.3\\src\\include\\**"
            ],
            "defines": [
                "_DEBUG",
                "UNICODE",
                "_UNICODE"
            ],
            "compilerPath": "C:\\swdepot\\msys64\\mingw64\\bin\\gcc.exe",
            "cStandard": "c17",
            "cppStandard": "c++17",
            "intelliSenseMode": "gcc-x64"
        }
    ],
    "version": 4
}
```

---------
**.**
