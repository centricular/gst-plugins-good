pulse_sources = [
  'plugin.c',
  'pulsesink.c',
  'pulsesrc.c',
  'pulsedeviceprovider.c',
  'pulseutil.c',
]

gstpulse = library('gstpulse',
  pulse_sources,
  c_args : gst_plugins_good_args,
  include_directories : gst_plugins_good_incs,
  dependencies : [gstbase_dep, gstaudio_dep, gstpbutils_dep, libpulse_dep],
  install : true,
  install_dir : plugins_install_dir,
)
