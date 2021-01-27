project(QtPropertyBrowser)
cmake_minimum_required(VERSION 3.6)

find_package(Qt5 COMPONENTS Core Widgets Gui)

set(qtpropertybrowser_srcs
    src/objectcontroller.cpp
    src/qtbuttonpropertybrowser.cpp
    src/qteditorfactory.cpp
    src/qtpropertybrowser.cpp
    src/qtpropertybrowserutils.cpp
    src/qtpropertymanager.cpp
    src/qttreepropertybrowser.cpp
    src/qtvariantproperty.cpp
)

set(qtpropertybrowser_resources
    src/qtpropertybrowser.qrc)
    

add_library(QtPropertyBrowser ${qtpropertybrowser_srcs} ${qtpropertybrowser_resources})
set_target_properties(QtPropertyBrowser PROPERTIES AUTOMOC ON AUTORCC ON)
target_link_libraries(QtPropertyBrowser Qt5::Core Qt5::Gui Qt5::Widgets)


