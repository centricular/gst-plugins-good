gstcairo = library('gstcairo',
  'gstcairo.c', 'gstcairooverlay.c',
  c_args : gst_plugins_good_args,
  include_directories : gst_plugins_good_incs,
  dependencies : [gstbase_dep, gstvideo_dep, cairo_dep],
  install : true,
  install_dir : plugins_install_dir,
)
