# Copyright 2018 Mike Dev
# Distributed under the Boost Software License, Version 1.0.
# See accompanying file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 3.5)
project(BoostForeach LANGUAGES CXX)

add_library(boost_foreach INTERFACE)
add_library(Boost::foreach ALIAS boost_foreach)

target_include_directories(boost_foreach INTERFACE include)

target_link_libraries(boost_foreach
    INTERFACE
        Boost::config
        Boost::core
        Boost::iterator
        Boost::mpl
        Boost::range
        Boost::type_traits
)
