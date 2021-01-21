# IDA Pattern Maker
A simple plugin that lets you generate patterns for code in IDA 7.5. 

Forked from mastahg and cursey. Updated to use IDA 7.5 SDK. 
The cmake files in this project were retrieved from 0xeb's repo [ida-cmake](https://github.com/0xeb/ida-cmake). 

IDA 7.5 has a drastically modified version of the SDK for version 7.5+, so this plugin required some overhaul. Sample code from the plugins folder in the 7.5 SDK was used as templates for this project.

## Usage

### Environment Variables

#### IDASDK

This is the directory where the IDA SDK is unpacked to. Set in Windows Powershell (per session) using:

```
$env:IDASDK = '<idasdk directory>'
```

#### IDABIN

Optional. This points to the directory of the IDA executable or the AppData folder so a copy of the plugin can be copied. If it doesn't exist, the plugin will be copied to `[IDASDK]/bin`. Set in Windows Powershell using: 

```
$env:IDABIN = '<ida binary directory>'
```

## Build Requirements
* IDA 7.5 SDK 
* Visual Studio (cmake projects are currently pretty specific to VS)
* CMake (3.2 version minimum)

## Build

### ida64.exe

```
mkdir build
cd build
cmake -A x64 .. -DEA64=YES
cmake --build . --config Release
```

### ida.exe

```
mkdir build
cd build
cmake -A x64 .. -DEA64=NO
cmake --build . --config Release
```