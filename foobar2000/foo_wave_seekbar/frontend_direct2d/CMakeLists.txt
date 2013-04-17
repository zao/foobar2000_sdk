set(D2D_SOURCES
	"Direct2D1.cc"
	"EntrypointD2D.cc"
	"Direct2D.h"
)

add_library(frontend_direct2d SHARED
	${D2D_SOURCES}
)

target_link_libraries(frontend_direct2d
	pfc
	waveform_sdk
	"d2d1.lib"
	debug
	"libboost_filesystem-mt-sgd.lib"
	"libboost_system-mt-sgd.lib"
	"libboost_thread-mt-sgd.lib"
	optimized
	"libboost_filesystem-mt-s.lib"
	"libboost_system-mt-s.lib"
	"libboost_thread-mt-s.lib"
)
deploy_component(frontend_direct2d foo_wave_seekbar)