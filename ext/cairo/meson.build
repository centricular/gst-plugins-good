gstcairo = library('gstcairo',
  'gstcairo.c', 'gstcairooverlay.c',
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstvideo_dep, cairo_dep],
  install : true,
  install_dir : plugins_install_dir,
)
