#Copyright (c) Microsoft. All rights reserved.
#Licensed under the MIT license. See LICENSE file in the project root for full license information.

cmake_minimum_required(VERSION 2.8.11)

compileAsC11()
set(theseTestsName mqtt_codec_ut)

set(${theseTestsName}_test_files
${theseTestsName}.c
)

set(${theseTestsName}_c_files
../../src/mqtt_codec.c
${SHARED_UTIL_REAL_TEST_FOLDER}/real_buffer.c
)

set(${theseTestsName}_h_files
)

include_directories(${MQTT_SRC_FOLDER})

build_c_test_artifacts(${theseTestsName} ON "tests/umqtt_tests")
