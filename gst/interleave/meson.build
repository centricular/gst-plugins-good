gstinterleave = library('gstinterleave',
  'plugin.c', 'interleave.c', 'deinterleave.c',
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstaudio_dep],
  install : true,
  install_dir : plugins_install_dir,
)
