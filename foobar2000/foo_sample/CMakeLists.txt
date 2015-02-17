include_directories(${WTL_INCLUDE_DIRS})

set(SAMPLE_SOURCES
	"contextmenu.cpp"
	"decode.cpp"
	"dsp.cpp"
	"initquit.cpp"
	"input_raw.cpp"
	"main.cpp"
	"mainmenu.cpp"
	"PCH.cpp"
	"playback_state.cpp"
	"preferences.cpp"
	"resource.h"
	"stdafx.h"
	"ui_element.cpp"
)

add_definitions(-Zm300)
enable_precompiled_headers("stdafx.h" SAMPLE_SOURCES)
add_library(foo_sample SHARED ${SAMPLE_SOURCES})
target_link_libraries(foo_sample
	foobar2000_component_client
	helpers
	pfc
	SDK
	shared
)
deploy_component(foo_sample foo_sample)