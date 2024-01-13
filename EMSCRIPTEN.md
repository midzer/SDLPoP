# Emscripten

## Compile

```
mkdir build && cd build
emcmake cmake ..
emmake make
```

## Link

```
emcc -fno-rtti -fno-exceptions -flto -O3 *.o -o index.html -sUSE_SDL=2 -sUSE_SDL_IMAGE=2 -sSDL2_IMAGE_FORMATS='["png"]' -sASYNCIFY -sASYNCIFY_ONLY=@funcs.txt -sASYNCIFY_IMPORTS=["invoke_iiii","invoke_v","invoke_vi"] -sASYNCIFY_IGNORE_INDIRECT -sENVIRONMENT=web --preload-file SDLPoP.ini --preload-file data/ --closure 1
```
