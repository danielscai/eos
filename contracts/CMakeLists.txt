# will be implictly used for any compilation unit if not overrided by SYSTEM_INCLUDE_FOLDERS parameter
# these directories go as -isystem <dir> to avoid warnings from code of third-party libraries
set(DEFAULT_SYSTEM_INCLUDE_FOLDERS ${CMAKE_SOURCE_DIR}/contracts/libc++/upstream/include ${CMAKE_SOURCE_DIR}/contracts/musl/upstream/include ${Boost_INCLUDE_DIR})

set(STANDARD_INCLUDE_FOLDERS ${CMAKE_SOURCE_DIR}/contracts)

add_subdirectory(eosiolib)
add_subdirectory(musl)
add_subdirectory(libc++)
add_subdirectory(multi_index_test)

add_subdirectory(eosio.system)
add_subdirectory(identity)
add_subdirectory(currency)
add_subdirectory(stltest)
#add_subdirectory(bancor)
#add_subdirectory(eosio.system)
add_subdirectory(asserter)
#add_subdirectory(exchange)
add_subdirectory(infinite)
add_subdirectory(proxy)
add_subdirectory(test_api)
add_subdirectory(test_api_mem)
add_subdirectory(test_api_db)
#add_subdirectory(simpledb)
#add_subdirectory(storage)
#add_subdirectory(social)
add_subdirectory(test.system)
add_subdirectory(noop)

install( DIRECTORY eosiolib DESTINATION include/ )
install( DIRECTORY skeleton DESTINATION share/ )
