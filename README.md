# Crosswalk Extensions for "two-in-one" hybrid Devices

Crosswalk extensions to support laptops with detachable or foldable keyboards. Currently only Windows versions 8.x and 10 are supported.

## Build and run demo from source

Requirements:
* Microsoft Visual Studio 2015
* Git for Windows

1. Create a directory to hold everything. We will refer to the *absolute path* of this directory using the ``<crosswalk>`` placeholder in the future.

```
> mkdir crosswalk
> cd crosswalk
```

2. Download crosswalk from https://download.01.org/crosswalk/releases/crosswalk/windows/beta/latest/ and unzip it, e.g. crosswalk64-19.49.514.4.zip. Make sure not to end up with nested directories after unpacking.

```
> dir

 Directory of <crosswalk>

22/03/2016  15:02    <DIR>          crosswalk64-19.49.514.4
22/03/2016  14:38        37,911,343 crosswalk64-19.49.514.4.zip
```

3. Clone the repository.

```
> git clone https://github.com/crosswalk-project/crosswalk-extensions-twoinone.git
> cd crosswalk-extensions-twoinone
```

4. Open ``twoinone-windows\twoinone.sln`` in Visual Studio 2015 and build the solution.

5. Enter demo dir and run the demo.

```
> cd demo-posture
> ..\..\crosswalk64-19.49.514.4\xwalk.exe --external-extensions-path=<crosswalk>\crosswalk-extensions-twoinone\twoinone-windows\bin\Debug --enable-inspector --enable-logging -v=1 app\manifest.json
```