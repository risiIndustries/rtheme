plugins = []

if get_option('plugin_gtk4').enabled()
  plugins += 'gtk4.py'
endif

if get_option('plugin_gtk3').enabled()
  plugins += 'gtk3.py'
endif

if get_option('plugin_gnome').enabled()
  subdir('gnome_shell')
endif

py.install_sources(plugins, subdir: 'rthemelib' / 'plugins')