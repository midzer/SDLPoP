# Emscripten

## Compile

```
mkdir build && cd build
emcmake cmake ..
emmake make
```

## Link

```
emcc -flto -O3 *.o -o index.html -sUSE_SDL=2 -sUSE_SDL_IMAGE=2 -sSDL2_IMAGE_FORMATS='["png"]' -sASYNCIFY -sENVIRONMENT=web --preload-file SDLPoP.ini --preload-file data/ --closure 1
```
