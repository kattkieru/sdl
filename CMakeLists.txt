
set( SDL sdl-1.2.15 )

file(
	GLOB SDL_SOURCES
	${SDL}/src/*.c
	${SDL}/src/audio/*.c
	${SDL}/src/audio/disk/*.c
	${SDL}/src/audio/dummy/*.c
	${SDL}/src/audio/windib/*.c
	${SDL}/src/audio/windx5/*.c
	${SDL}/src/cdrom/*.c
	${SDL}/src/cdrom/win32/*.c
	${SDL}/src/cpuinfo/*.c
	${SDL}/src/events/*.c
	${SDL}/src/file/*.c
	${SDL}/src/joystick/*.c
	${SDL}/src/joystick/win32/*.c
	${SDL}/src/loadso/win32/*.c
	${SDL}/src/stdlib/*.c
	${SDL}/src/thread/*.c
	${SDL}/src/thread/generic/*.c
	${SDL}/src/thread/win32/*.c
	${SDL}/src/timer/*.c
	${SDL}/src/timer/win32/*.c
	${SDL}/src/video/*.c
	${SDL}/src/video/dummy/*.c
	${SDL}/src/video/wincommon/*.c
	${SDL}/src/video/windib/*.c
	${SDL}/src/video/windx5/*.c
)

add_library( sdl ${SDL_SOURCES} )
target_include_directories( sdl PUBLIC ${SDL}/include )

add_library( sdlmain ${SDL}/src/main/win32/SDL_win32_main.c )
target_include_directories( sdlmain PUBLIC ${SDL}/include )
