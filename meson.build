project(
	'renderman',
	'cpp',
  version : '0.1',
  default_options : [
  	'warning_level=3',
    'cpp_std=c++14'
  ]
)

subdir('src')

deps = [
  # OpenGL
  dependency('gl', required: true),
  dependency('glut', required: true),
	# GLFW3 Dependency. Enable install, and affix version.
  dependency('glfw3', version: '3.3.8' , required: true, default_options: ['install=true']),
  # GLEW (GL Extension Wrangler)
  dependency('glew', static: true),
]

exe = executable(
  'renderman',
  sources,
  dependencies: deps,
  install : true
)

test('basic', exe)
