add_library(shared STATIC IMPORTED GLOBAL
)
add_library(shared-headers STATIC
	"audio_math.h"
	"filedialogs.h"
	"shared.h"
	"win32_misc.h"
)
set_target_properties(shared-headers PROPERTIES
	LINKER_LANGUAGE CXX
)

set_target_properties(shared PROPERTIES
	IMPORTED_LOCATION ${CMAKE_CURRENT_SOURCE_DIR}/shared.lib
)