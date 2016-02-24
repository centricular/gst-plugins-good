gsticydemux = library('gsticydemux',
  'gsticydemux.c',
  c_args : gst_plugins_good_args,
  include_directories : gst_plugins_good_incs,
  dependencies : [gst_dep, gstbase_dep, gsttag_dep, zlib_dep],
  install : true,
  install_dir : plugins_install_dir,
)
