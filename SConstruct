orig_libs = [
'X11',
'GL',
'GLEW',
'glfw3',
#'openvr_api',
]


libs=[
'Xi', 'GLEW', 'GLU', 'm', 'GL', 'm', 'pthread', 'dl', 'drm', 'Xdamage', 'X11-xcb', 'xcb-glx', 'xcb-dri2', 'glfw3', 'rt', 'm', 'dl', 'Xrandr', 'Xinerama', 'Xxf86vm', 'Xext', 'Xcursor', 'Xrender', 'Xfixes', 'X11', 'pthread', 'xcb', 'Xau', 'Xdmcp', 'openvr_api'
]

lib_path = ['/usr/lib', '/usr/local/lib', 'openvr/lib/linux64']
include_path = ['glhpp', 'openvr/headers', '/usr/local/include/GLFW']

CCFLAGS   = "-g -std=c++0x"
LINKFLAGS = " `pkg-config --static --libs x11 xrandr xi xxf86vm glew glfw3 ` "

#env = Environment(CCFLAGS=CCFLAGS, LINKFLAGS=LINKFLAGS, CPPPATH=include_path, LIBPATH=lib_path, LIBS=orig_libs)
env = Environment(CCFLAGS=CCFLAGS, LINKFLAGS=LINKFLAGS, CPPPATH=include_path, LIBPATH=lib_path, LIBS=libs)
#env = Environment( CPPPATH=include_path , LIBPATH=lib_path, LIBS=libs)

env.Program('hello.cpp'
        #'openvr/bin/linux64/libopenvr_api.a',
        #'openvr/bin/linux64/libopenvr_api.so',
        )
