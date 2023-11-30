# Emscripten

Note: -flto CXX flag not working for RA, not used for both

## Build

```
mkdir build && cd build
emcmake cmake ..
```

## Link

### TD

```
em++ -O3 *.o ../../../common/libcommon.a ../../../common/libcommonv.a -o index.html -sUSE_SDL=2 -lopenal -sASYNCIFY -sINITIAL_MEMORY=128MB -sENVIRONMENT=web --preload-file DEMO.MIX --preload-file DEMOL.MIX --preload-file DEMOM.MIX --preload-file SOUNDS.MIX --preload-file SPEECH.MIX --preload-file conquer.ini --preload-file rules.ini --closure 1
```

### RA

```
em++ -O3 *.o ../../../common/libcommon.a ../../../common/libcommonv.a -o index.html -sUSE_SDL=2 -lopenal -sASYNCIFY -sINITIAL_MEMORY=128MB -sENVIRONMENT=web --preload-file MAIN.MIX --preload-file REDALERT.MIX --preload-file redalert.ini --closure 1
```
