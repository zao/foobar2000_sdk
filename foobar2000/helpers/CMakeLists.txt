set(HELPERS_SOURCES
	"album_art_helpers.h"
	"bitreader_helper.h"
	"CallForwarder.h"
	"cfg_guidlist.h"
	"clipboard.cpp"
	"clipboard.h"
	"COM_utils.h"
	"create_directory_helper.cpp"
	"create_directory_helper.h"
	"cuesheet_index_list.cpp"
	"cuesheet_index_list.h"
	"cue_creator.cpp"
	"cue_creator.h"
	"cue_parser.cpp"
	"cue_parser.h"
	"cue_parser_embedding.cpp"
	"dialog_resize_helper.cpp"
	"dialog_resize_helper.h"
	"dropdown_helper.cpp"
	"dropdown_helper.h"
	"dynamic_bitrate_helper.cpp"
	"dynamic_bitrate_helper.h"
	"filetimetools.cpp"
	"filetimetools.h"
	"file_cached.h"
	"file_info_const_impl.cpp"
	"file_info_const_impl.h"
	"file_list_helper.cpp"
	"file_list_helper.h"
	"file_move_helper.cpp"
	"file_move_helper.h"
	"file_win32_wrapper.h"
	"file_wrapper_simple.cpp"
	"file_wrapper_simple.h"
	"helpers.h"
	"icon_remapping_wildcard.h"
	"IDataObjectUtils.cpp"
	"IDataObjectUtils.h"
	"input_helpers.cpp"
	"input_helpers.h"
	"listview_helper.cpp"
	"listview_helper.h"
	"metadb_io_hintlist.cpp"
	"metadb_io_hintlist.h"
	"meta_table_builder.h"
	"mp3_utils.cpp"
	"mp3_utils.h"
	"playlist_position_reference_tracker.h"
	"ProfileCache.h"
	"seekabilizer.cpp"
	"seekabilizer.h"
	"StdAfx.h"
	"stream_buffer_helper.cpp"
	"stream_buffer_helper.h"
	"string_filter.h"
	"text_file_loader.cpp"
	"text_file_loader.h"
	"ThreadUtils.h"
	"VisUtils.cpp"
	"VisUtils.h"
	"wildcard.cpp"
	"wildcard.h"
	"win32_dialog.cpp"
	"win32_dialog.h"
	"win32_misc.cpp"
	"win32_misc.h"
	"window_placement_helper.cpp"
	"window_placement_helper.h"
)

add_definitions(-Zm300)
enable_precompiled_headers("StdAfx.h" HELPERS_SOURCES)
add_library(helpers STATIC ${HELPERS_SOURCES})