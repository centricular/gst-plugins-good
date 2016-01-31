flxdec = library('gstflxdec',
  'gstflxdec.c', 'flx_color.c',
  c_args : gst_plugins_good_args,
  include_directories : gst_plugins_good_incs,
  dependencies : [gstbase_dep, gst_dep],
  install : true,
  install_dir : plugins_install_dir,
)
