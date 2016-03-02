soup_sources = [
  'gstsouphttpsrc.c',
  'gstsouphttpclientsink.c',
  'gstsouputils.c',
  'gstsoup.c',
]

soup_args = [
  '-DSOUP_VERSION_MIN_REQUIRED=SOUP_VERSION_2_26',
  '-DSOUP_VERSION_MAX_ALLOWED=SOUP_DEPRECATED_IN_2_26',
]

libsoup_dep = dependency('libsoup-2.4', version : '>=2.40', required : false)

if libsoup_dep.found()
  gstsouphttpsrc = library('gstsouphttpsrc',
    soup_sources,
    c_args : gst_plugins_good_args + soup_args,
    include_directories : gst_plugins_good_incs,
    dependencies : [gstbase_dep, gsttag_dep, libsoup_dep],
    install : true,
    install_dir : plugins_install_dir,
  )
endif
