png_sources = [
  'gstpng.c',
  'gstpngenc.c',
  'gstpngdec.c',
]

gstpng = library('gstpng',
  png_sources,
  c_args : gst_plugins_good_args,
  include_directories : gst_plugins_good_incs,
  dependencies : [gstbase_dep, gstvideo_dep, libpng_dep],
  install : true,
  install_dir : plugins_install_dir,
)
