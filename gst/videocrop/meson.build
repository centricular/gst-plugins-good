gstvideocrop = library('gstvideocrop',
  'gstvideocrop.c', 'gstaspectratiocrop.c',
  c_args : gst_plugins_good_args,
  include_directories : gst_plugins_good_incs,
  dependencies : [gstbase_dep, gstvideo_dep],
  install : true,
  install_dir : plugins_install_dir,
)
