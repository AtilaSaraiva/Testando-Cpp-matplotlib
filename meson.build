project('usematplotlibcpp', 'cpp',
  version : '0.1',
  default_options : ['warning_level=3',
                     'cpp_std=c++14'])


cmake = import('cmake')

tensorflow_dep = dependency('tensorflow')
matplotlibcpp_proj = cmake.subproject('matplotlibcpp')
matplotlibcpp_lib = matplotlibcpp_proj.dependency('matplotlib_cpp')


exe = executable('usematplotlibcpp', 'teste.cpp',
        dependencies : [matplotlibcpp_lib],
        install : true)


test('basic', exe)
