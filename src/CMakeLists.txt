#  Copyright 2019 U.C. Berkeley RISE Lab
# 
#  Licensed under the Apache License, Version 2.0 (the "License");
#  you may not use this file except in compliance with the License.
#  You may obtain a copy of the License at
# 
#      http://www.apache.org/licenses/LICENSE-2.0
# 
#  Unless required by applicable law or agreed to in writing, software
#  distributed under the License is distributed on an "AS IS" BASIS,
#  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#  See the License for the specific language governing permissions and
#  limitations under the License.

CMAKE_MINIMUM_REQUIRED(VERSION 3.6 FATAL_ERROR)

SET(KV_LIBRARY_DEPENDENCIES
    protobuf
    anna-proto
    pthread
    zmq
    hydro-zmq
    yaml-cpp
)

SET(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/target/kvs)

ADD_SUBDIRECTORY(hash_ring)
ADD_SUBDIRECTORY(kvs)
ADD_SUBDIRECTORY(monitor)
ADD_SUBDIRECTORY(route)
ADD_SUBDIRECTORY(benchmark)
