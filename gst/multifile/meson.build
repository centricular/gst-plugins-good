multifile_sources = [
  'gstmultifilesink.c',
  'gstmultifilesrc.c',
  'gstmultifile.c',
  'gstsplitfilesrc.c',
  'gstsplitmuxpartreader.c',
  'gstsplitmuxsink.c',
  'gstsplitmuxsrc.c',
  'gstsplitutils.c',
  'patternspec.c',
]

gstmultifile = library('gstmultifile',
  multifile_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [ gstvideo_dep, gstbase_dep, gio_dep ],
  install : true,
  install_dir : plugins_install_dir,
)

test_splitmuxpartreader_sources = [
  'test-splitmuxpartreader.c',
  'gstsplitmuxpartreader.c',
  'gstsplitmuxsrc.c',
  'gstsplitutils.c',
  'patternspec.c',
]

executable('test-splitmuxpartreader',
  test_splitmuxpartreader_sources,
  include_directories : core_incs,
  c_args : core_args,
  dependencies : [ gsttag_dep, gstbase_dep ],
  install : false,
)
