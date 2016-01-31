flac_sources = [
  'gstflac.c',
  'gstflacdec.c',
  'gstflacenc.c',
  'gstflactag.c',
]

gstflac = library('gstflac',
  flac_sources,
  c_args : gst_plugins_good_args + ['-DGST_USE_UNSTABLE_API'],
  include_directories : gst_plugins_good_incs,
  dependencies : [gstbase_dep, gsttag_dep, gstaudio_dep, flac_dep],
  install : true,
  install_dir : plugins_install_dir,
)
