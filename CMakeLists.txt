cmake_minimum_required(VERSION 3.16)
project(Jeopardy VERSION 1.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt6 REQUIRED COMPONENTS Core Gui Widgets Xml Multimedia MultimediaWidgets)

add_executable(jeopardy
    main.cpp
    jeopardy.cpp
    player.cpp
    gamefield.cpp
    answer.cpp
    editor.cpp
    podium.cpp
    doublejeopardy.cpp
    jeopardy.h
    player.h
    gamefield.h
    answer.h
    editor.h
    podium.h
    doublejeopardy.h
    answer.ui
)

target_link_libraries(jeopardy
    Qt6::Core
    Qt6::Gui
    Qt6::Widgets
    Qt6::Xml
    Qt6::Multimedia
    Qt6::MultimediaWidgets
)
