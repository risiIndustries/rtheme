pkgdatadir = join_paths(get_option('prefix'), get_option('datadir'))
moduledir = join_paths(pkgdatadir, 'rthemed')

python = import('python')

conf = configuration_data()
conf.set('PYTHON', python.find_installation('python3').full_path())
conf.set('pkgdatadir', pkgdatadir)
configure_file(
  input: 'rthemed.in',
  output: 'rthemed',
  configuration: conf,
  install: true,
  install_dir: get_option('bindir')
)

sources = [
  '__init__.py',
  '__main__.py',
  'main.py',
  'daemon.py',
]

subdir('systemd')

install_data(sources, install_dir: moduledir)