#!/usr/bin/env python
import os
env = SConscript("godot-cpp/SConstruct")

env.Append(CPPPATH=["src/"])
sources = Glob("src/godot/*.cpp") + Glob("src/sim/*.cpp")

library = env.SharedLibrary(
    "bin/libnujoom{}{}".format(env["suffix"], env["SHLIBSUFFIX"]),
    source=sources,
)
Default(library)
