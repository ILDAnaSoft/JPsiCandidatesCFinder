#######################################################
# cmake file for building JPsiCandidatesCFinder analysis package
# @author Ete Remi, DESY
#######################################################

# -------------------------------------------------
# include directories
include_directories( BEFORE include )

# -------------------------------------------------
# build the project library
# This compiles everything in the src directory and build a library
# called libJPsiCandidatesCFinder.so, that with be install in the lib directory
# in the top level directory of your project 
aux_source_directory( src SRC_FILES )
add_shared_library( ${PROJECT_NAME} ${SRC_FILES} )
install( TARGETS ${PROJECT_NAME} LIBRARY DESTINATION lib )
