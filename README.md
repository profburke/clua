
## CLua


## NOTE: the following is the README for Moonbird, not CLua. Will be corrected soon.

Import Lua into Swift.

This module allows you to call the Lua API from Swift, but
the only thing that is available is the bare C API. If you want a
*Swiftier* interface, take a look at the [Moonbird](https://github.com/profburke/moonbird) module.

#### Usage

This module is designed to work with the Swift Package Manager (SPM). In order to use this module you need to do two things:

1. Include `CLua` as a dependency in your `Pacakage.swift` file.
2. Import the module as needed in your Swift source.

An example follows:

###### Package.swift
    let package = Package(
        name: "Sample",
        dependencies: [
          .Package(url: "https://github.com/profburke/clua", majorVersion: 1),
        ]
     )

##### Sample.swift
    import CLua
    
    var L = LuaState()
    


#### TODO

Between various Lua versions (5.1, 5.2, 5.3) and various packaging/naming conventions for different OS distros, the Lua include files and library may not always be in the locations assumed in this code.

It would be nice to have some auto-configure as part of the build process, but at the moment, I'm not sure how to get that to play nicely with the Swift Package Manager. If you have an idea, pull requests greatly appreciated! (*Or opening an issue, would be appreciated as well.*)


#### License

**CLua**

Copyright © 2016 Matthew M. Burke

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.



