vbox_c = configure_file(input : 'gstvideoboxorc-dist.c',
  output : 'gstvideoboxorc.c',
  configuration : configuration_data()
)

vbox_h = configure_file(input : 'gstvideoboxorc-dist.h',
  output : 'gstvideoboxorc.h',
  configuration : configuration_data()
)

gstvideobox = library('gstvideobox',
  'gstvideobox.c', vbox_c,
  c_args : gst_plugins_good_args,
  include_directories : gst_plugins_good_incs,
  dependencies : [orc_dep, gstbase_dep, gstvideo_dep],
  install : true,
  install_dir : plugins_install_dir,
)
