project(
	'wfp',
    'c',
	'cpp',
	version: '0.1',
	meson_version: '>=0.51.0',
	default_options: [
		'cpp_std=c++17',
        'c_std=c11',
		'warning_level=2',
		'werror=false',
	],
)

wayfire = dependency('wayfire')
wlroots = dependency('wlroots')
wfconfig = dependency('wf-config')

add_project_arguments(['-DWLR_USE_UNSTABLE'], language: ['cpp', 'c'])
add_project_arguments(['-DWAYFIRE_PLUGIN'], language: ['cpp', 'c'])
add_project_arguments(['-I/usr/include/pixman-1'], language: 'cpp')
add_project_arguments(['-I/usr/include/cairo'], language: 'cpp')
add_project_link_arguments(['-rdynamic'], language:'cpp')

subdir('src')
subdir('metadata')

summary = [
	'',
	'----------------',
	'wfp @0@'.format(meson.project_version()),
	'----------------',
	''
]
message('\n'.join(summary))
