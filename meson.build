project('igcl', 'cpp')

compiler = meson.get_compiler('cpp')
link_deps = []

incdirs = ['include']
cflags = []

sources = [
  'src/cApiWrapper.cpp',
]

incdirs = include_directories(incdirs)

igcl = static_library(
    'igcl',
    sources,
    cpp_args: cflags,
    include_directories: incdirs,
    dependencies: link_deps,
)
igcl_dep = declare_dependency(
    include_directories: incdirs,
    dependencies: link_deps,
    link_with: igcl,
    version: meson.project_version()
)

meson.override_dependency('igcl', igcl_dep)

# vim: set ts=4 sts=4 sw=4 et:
