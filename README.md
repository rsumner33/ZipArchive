#ZipArchive

ZipArchive is a simple utility class for zipping and unzipping files on iOS and Mac.

##How to add ZipArchive to your project

1. Add the `ZipArchive` and `minizip` folders to your project.
2. Add the `libz` library to your target

ZipArchive requires ARC.

###Usage
```objective-c
// Unzip Operation
NSString *zipPath = @"path_to_your_zip_file";
NSString *destinationPath = @"path_to_the_folder_where_you_want_it_unzipped";
    
[Main unzipFileAtPath:zipPath 
        toDestination:destinationPath];
    
// Zip Operation
NSString *zippedPath = @"path_where_you_want_the_file_created";
NSArray *inputPaths = @[[[NSBundle mainBundle] pathForResource:@"photo1" ofType:@"jpg"],
                        [[NSBundle mainBundle] pathForResource:@"photo1" ofType:@"jpg"]];
    
[Main createZipFileAtPath:zippedPath
         withFilesAtPaths:inputPaths];
    
// Zip Directory
[Main createZipFileAtPath:zippedPath
  withContentsOfDirectory:inputPaths];
```

###Licensing
ZipArchive is released under the [MIT license](https://github.com/ZipArchive/ZipArchive/raw/master/LICENSE) and our slightly modified version of [Minizip](http://www.winimage.com/zLibDll/minizip.html) 1.1 is licensed under the [Zlib license](http://www.zlib.net/zlib_license.html).
