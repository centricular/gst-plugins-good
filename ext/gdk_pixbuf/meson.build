pixbuf_sources = [
  'gstgdkpixbufdec.c',
  'gstgdkpixbufoverlay.c',
  'gstgdkpixbufplugin.c',
  'gstgdkpixbufsink.c',
]

gdkpixbuf_dep = dependency('gdk-pixbuf-2.0', version : '>=2.8.0', required : false)

if gdkpixbuf_dep.found()
  gstgdkpixbuf = library('gstgdkpixbuf',
    pixbuf_sources,
    c_args : gst_plugins_good_args,
    include_directories : gst_plugins_good_incs,
    dependencies : [gstbase_dep, gstvideo_dep, gstcontroller_dep, gdkpixbuf_dep],
    install : true,
    install_dir : plugins_install_dir,
  )
endif
