udp_sources = [
  'gstudp.c',
  'gstudpsrc.c',
  'gstudpsink.c',
  'gstmultiudpsink.c',
  'gstdynudpsink.c',
  'gstudpnetutils.c'
]

gstudp = library('gstudp',
  udp_sources,
  c_args : gst_plugins_good_args,
  include_directories : gst_plugins_good_incs,
  dependencies : [gstbase_dep, gstnet_dep, gio_dep],
  install : true,
  install_dir : plugins_install_dir,
)
