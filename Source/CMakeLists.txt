set(TargetName Data2Array)
add_executable(${TargetName} Main.cpp ../CMake/Data2Array.cmake)

if (Data2Array_FOLDER)
    set_property(TARGET ${TargetName} PROPERTY FOLDER "${Data2Array_FOLDER}")
endif()


if (MSVC)
    set_target_properties(
        ${TargetName} 
        PROPERTIES 
        VS_DEBUGGER_WORKING_DIRECTORY  
        ${CMAKE_CURRENT_SOURCE_DIR}
    )
endif()
