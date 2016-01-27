vpx_sources = [
  'gstvp8dec.c',
  'gstvp8enc.c',
  'gstvp8utils.c',
  'gstvp9dec.c',
  'gstvp9enc.c',
  'gstvpxdec.c',
  'gstvpxenc.c',
  'plugin.c',
]

vpx_features = [
  [ 'vpx/vp8cx.h', 'vpx_codec_vp8_cx_algo', '-DHAVE_VP8_ENCODER' ],
  [ 'vpx/vp8dx.h', 'vpx_codec_vp8_dx_algo', '-DHAVE_VP8_DECODER' ],
  [ 'vpx/vp8cx.h', 'vpx_codec_vp9_cx_algo', '-DHAVE_VP9_ENCODER' ],
  [ 'vpx/vp8dx.h', 'vpx_codec_vp9_dx_algo', '-DHAVE_VP9_DECODER' ],
]

vpx_args = [ ]

foreach f : vpx_features
  header = f.get(0)
  codec_iface = f.get(1)
  extra_define = f.get(2)
  link_code = '#include <@0@>\nint main (int a, char ** g) { const vpx_codec_iface_t *c = &@1@; return c != 0; }'.format(header,codec_iface)
  # FIXME: should take dependencies : vpx_dep argument
  if cc.links(link_code, args : '-lvpx')
    vpx_args += extra_define
  endif
endforeach

if vpx_args.length() == 0
  message('WARNING: libvpx was built without any encoder or decoder features!')
endif

if dependency('vpx', version : '>= 1.4.0').found()
  vpx_args += '-DHAVE_VPX_1_4'
endif

gstvpx = library('gstvpx',
  vpx_sources,
  c_args : core_args + vpx_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gsttag_dep, gstvideo_dep, vpx_dep],
  install : true,
  install_dir : plugins_install_dir,
)
