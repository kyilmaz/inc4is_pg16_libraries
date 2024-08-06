# inc4is_pg16_libraries
 postgresql 16.3 libraries copy for doing code analysis
 (h) librares for intellisense for windows

 All *.h files are copied from Rocky Linux 8 that runs pg16.3.
 for just analysis/read the codes not for applicable to build or debug or any kind of..
 the files are required for postgresql-16 code analysis.

 Firstly should install MSYS & mingw & gpp etc

 [r2h]:https://code.visualstudio.com/docs/cpp/config-mingw

 msys & mingw releated dirs must be located on c:\swdepot dir
 After MSYS & mingw setups are completed apply below steps 

```bash
$ cd /c/swdepot

$ wget https://ftp.postgresql.org/pub/source/v16.3/postgresql-16.3.tar.gz

$ tar -xf postgresql-16.3.tar.gz
```
 Copy these Repo to localy via Windows CMD
```console
cd c:\swdepot
git clone https://github.com/kyilmaz/inc4is_pg16_libraries.git
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

And Change c_cpp_properties (for only using analysis stage)

---------
**.**
