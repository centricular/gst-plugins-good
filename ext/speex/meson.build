speex_sources =[
  'gstspeex.c',
  'gstspeexdec.c',
  'gstspeexenc.c',
]

gstspeex = library('gstspeex',
  speex_sources,
  c_args : gst_plugins_good_args + ['-DGST_USE_UNSTABLE_API'],
  include_directories : gst_plugins_good_incs,
  dependencies : [gstbase_dep, gsttag_dep, gstaudio_dep, speex_dep, libm],
  install : true,
  install_dir : plugins_install_dir,
)
