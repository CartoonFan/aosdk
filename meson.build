project('aosdk', 'cpp', version: '2.2', license: 'GPL-3.0-or-later',
        default_options: ['optimization=g',
                          'warning_level=3',
                          'cpp_std=c++20',
                          'b_coverage=true'])


inc = include_directories('include')


deps = dependency(['libKeyFinder',
                   'libavcodec',
                   'libavformat',
                   'libavutil',
                   'taglib',
                   'zlib'])

run_target('sonarqube_report',
           command: 'scripts/sonarqube_report.sh')


subdir('src')
subdir('include')
