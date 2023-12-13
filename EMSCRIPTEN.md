# Emscripten

## Compile

```
mkdir build && cd build
emcmake cmake ..
emmake make
```

## Link

```
emcc -fno-rtti -fno-exceptions -flto -O3 *.o -o index.html -sUSE_SDL=2 -sUSE_SDL_IMAGE=2 -sSDL2_IMAGE_FORMATS='["png"]' -sASYNCIFY -sASYNCIFY_ONLY=["main","update_screen","init_game","do_paused","draw_game_frame","redraw_screen","show_title","do_wait","do_simple_wait","fade_in_frame","start_game","load_intro","cutscene_2_6","proc_cutscene_frame","fade_out_frame","SDL_Delay","SDL_UpdateMouseFocus","GLES2_RenderPresent","Emscripten_GLES_SwapWindow","Emscripten_HandleMouseMove","dynCall_iiii","dynCall_v","dynCall_vi"] -sASYNCIFY_IMPORTS=["invoke_v","invoke_vi"] -sASYNCIFY_IGNORE_INDIRECT -sENVIRONMENT=web --preload-file SDLPoP.ini --preload-file data/ --closure 1
```
