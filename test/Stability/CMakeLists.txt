file(GLOB TestStabilityFiles ${CMAKE_CURRENT_SOURCE_DIR}/*.*)
get_property(IPOPT_FOUND GLOBAL PROPERTY IPOPT_FOUND)
if(NOT IPOPT_FOUND)
    list(REMOVE_ITEM TestStabilityFiles "${CMAKE_CURRENT_SOURCE_DIR}/Problem_LP_bigm.cpp")
    list(REMOVE_ITEM TestStabilityFiles "${CMAKE_CURRENT_SOURCE_DIR}/Problem_LP_bigm.h")
    list(REMOVE_ITEM TestStabilityFiles "${CMAKE_CURRENT_SOURCE_DIR}/Problem_LP_simple.cpp")
    list(REMOVE_ITEM TestStabilityFiles "${CMAKE_CURRENT_SOURCE_DIR}/Problem_LP_simple.h")
    list(REMOVE_ITEM TestStabilityFiles "${CMAKE_CURRENT_SOURCE_DIR}/Test_InterlockingSolver_Ipopt.cpp")
    list(REMOVE_ITEM TestStabilityFiles "${CMAKE_CURRENT_SOURCE_DIR}/Test_toymodel_Ipopt.cpp")
endif()
set(TestStabilityFiles ${TestStabilityFiles} PARENT_SCOPE)