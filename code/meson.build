json = subproject('json')

code_lib = static_library('code_lib', files('program.cpp'),
    include_directories: '.',
    dependencies: [json.get_variable('nlohmann_json_dep')],
    install: true)

code_dep = declare_dependency(
    link_with: code_lib,
    include_directories: '.')

executable('ham-radio', files('main.cpp'), dependencies: code_dep, install: true)
