gstximagesrc = library('gstximagesrc',
  'gstximagesrc.c', 'ximageutil.c',
  c_args : gst_plugins_good_args,
  include_directories : gst_plugins_good_incs,
  dependencies : [gstbase_dep, x_dep, xfixes_dep, xdamage_dep],
  install : true,
  install_dir : plugins_install_dir,
)
