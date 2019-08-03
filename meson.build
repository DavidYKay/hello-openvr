project('helloOpenVR', 'cpp',
  default_options : [
    #'c_std=c11',
      'cpp_std=c++14',
      #'cpp_stdlib=libc++',
      #'stdlib=libc++',
      ])

cpp_sources = [
  'hello.cpp',
]

#add_global_arguments('-stdlib=libc++', language: 'cpp')
#add_global_arguments('-Wno-all', language: 'cpp')

cc = meson.get_compiler('cpp')
# depois = dependency('OIS')
depfilament = declare_dependency(
  #compile_args: [ '-L lib' ],
  dependencies : [
    # cc.find_library('backend', dirs:['/home/dk/workspace/current/hello-filament/lib/x86_64',]),
    # cc.find_library('dl'),
    # cc.find_library('pthread'),
    # cc.find_library('libc++'),
    #dependency('filament'),
    dependency('x11'),
    dependency('xrandr'),
    dependency('xi'),
    dependency('xxf86vm'),
    dependency('glew'),
    dependency('glfw3'),
  ],
  include_directories: include_directories(
    #'include',
  )
)

openvr = declare_dependency(
  compile_args: ['-Wno-all'],
  dependencies : [
     cc.find_library('openvr_api', dirs:[
       '/home/dk/workspace/current/hello-openvr/openvr/lib/linux64',
     ]),
  ],
  include_directories: include_directories(
    'openvr/headers'
   )
  )

glhpp = declare_dependency(
  compile_args: [
    #'-Wno-sign-compare',
    '-Wno-all',
  ],
  include_directories: include_directories(
    'glhpp'
   )
  )


helloopenvr = executable('main', cpp_sources,
  link_with: [
    #libgl3w
  ],
  dependencies: [
    glhpp,
    openvr,
    dependency('GL'),
    dependency('glfw3'),

    #dependency('glu'),
    #dependency('glew'),
    #dependency('pthread'),
    #dependency('SDL2'),
  ],

  include_directories: include_directories(

  )
)
