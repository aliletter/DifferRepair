# PackageUpdata  [![](https://www.jitpack.io/v/mr-absurd/packageupdata.svg)](https://www.jitpack.io/#mr-absurd/packageupdata)
With the iterative update of the project, the function is more and more complicated, we develop application package is also more and more huge. If the user needs to update the application, the user must download a large installation package, which led to some users can not update the application. Therefore, it is necessary to reduce the installation package. PackageUpdata just helped us to achieve this function.
# How to
To get a Git project into your build:
## Step 1. Add the JitPack repository to your build file
Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
  
## Step 2. Add the dependency

	dependencies {
	        compile 'com.github.mr-absurd:packageupdata:v1.0.2'
	}
## Step 3. Set JniLibs directory

```Java
android {
    ...
    sourceSets {
        main() {
            jniLibs.srcDirs = ['libs']
        }
    }
}

```
## Step 4. Copy dynamic library file
Click here [dynamic library file](https://github.com/mr-absurd/packageupdata/tree/master/app/libs) ,copy the files to your application.

<br><br><br>
#Methods Recommend
```Java
    /*
     * oldfile: apkfile which install in your device on current
     * newfile: akpfile which is non-exist,and will be combined by the method
     * patchfile: patchfile and oldfile are combine newfile
     */
    PackageUpdata.bspatch(File oldfile,File newfile,File patchfile)
```
