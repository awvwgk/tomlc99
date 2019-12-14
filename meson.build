project('tomlc99', 'c')

tomlc99_lib = library(meson.project_name(), 'toml.c', install: true)
tomlc99_dep = declare_dependency(link_with: tomlc99_lib)
install_headers('toml.h')

tomlc99_cat = executable('@0@.cat'.format(meson.project_name()), 'toml_cat.c',
                         dependencies: tomlc99_dep)
tomlc99_json = executable('@0@.json'.format(meson.project_name()), 'toml_json.c',
                          dependencies: tomlc99_dep)

subdir('unittest')
