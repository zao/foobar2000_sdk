add_library(wtl-headers STATIC
	"atlapp.h"
	"atlcrack.h"
	"atlctrls.h"
	"atlctrlw.h"
	"atlctrlx.h"
	"atlddx.h"
	"atldlgs.h"
	"atldwm.h"
	"atlfind.h"
	"atlframe.h"
	"atlgdi.h"
	"atlmisc.h"
	"atlprint.h"
	"atlres.h"
	"atlresce.h"
	"atlribbon.h"
	"atlscrl.h"
	"atlsplit.h"
	"atltheme.h"
	"atluser.h"
	"atlwince.h"
	"atlwinx.h"
)
set_target_properties(wtl-headers PROPERTIES LINKER_LANGUAGE CXX)

set(WTL_INCLUDE_DIRS ${CMAKE_CURRENT_SOURCE_DIR} PARENT_SCOPE)