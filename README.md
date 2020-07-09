[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Build Status](https://github.com//AndreyAndreevich/conan-civetweb/workflows/CI/badge.svg))](https://github.com//AndreyAndreevich/conan-civetweb/actions)
[![Download](https://api.bintray.com/packages/andrbek/conan/civetweb%3Aandrbek/images/download.svg)](https://bintray.com/andrbek/conan/civetweb%3Aandrbek/_latestVersion)

# conan-prometheus-cpp

## Basic setup

    $ conan install . civetweb/1.12@andrbek/testing
    
## Project setup

If you handle multiple dependencies in your project is better to add a *conanfile.txt*
    
    [requires]
      civetweb/1.12@andrbek/testing

    [options]
      civetweb:shared=True                              # default is False
      civetweb:fPIC=True                                # default is True
      civetweb:enable_ssl=True                          # default is True
      civetweb:enable_websockets=True                   # default is True
      civetweb:enable_ipv6=True                         # default is True
      civetweb:enable_cxx=True                          # default is True

    [generators]
      cmake

Complete the installation of requirements for your project running:

    conan install .

Project setup installs the library (and all his dependencies) and generates the files *conanbuildinfo.cmake* with all the 
paths and variables that you need to link with your dependencies.
