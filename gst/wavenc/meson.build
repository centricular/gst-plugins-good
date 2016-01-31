gstwavenc = library('gstwavenc',
  'gstwavenc.c',
  c_args : gst_plugins_good_args,
  include_directories : gst_plugins_good_incs,
  dependencies : [gstbase_dep, gstaudio_dep, gstriff_dep],
  install : true,
  install_dir : plugins_install_dir,
)
