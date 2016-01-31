pixbuf_sources = [
  'gstgdkpixbufdec.c',
  'gstgdkpixbufoverlay.c',
  'gstgdkpixbufplugin.c',
  'gstgdkpixbufsink.c',
]

gstgdkpixbuf = library('gstgdkpixbuf',
  pixbuf_sources,
  c_args : gst_plugins_good_args,
  include_directories : gst_plugins_good_incs,
  dependencies : [gstbase_dep, gstvideo_dep, gstcontroller_dep, gdkpixbuf_dep],
  install : true,
  install_dir : plugins_install_dir,
)
