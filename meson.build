project('liba-aac', 'c', version: '1.6.2', license: 'MIT')

spa_dep = dependency('libspa-0.2', method: 'pkg-config')
fdk_aac_dep = dependency('fdk-aac', method: 'pkg-config')

spa_plugindir = spa_dep.get_variable('plugindir')

codec_args = ['-DCODEC_PLUGIN']

shared_library(
  'spa-codec-bluez5-aac',
  sources: ['a2dp-codec-aac.c', 'media-codecs.c'],
  c_args: codec_args,
  dependencies: [spa_dep, fdk_aac_dep],
  install: true,
  install_dir: spa_plugindir / 'bluez5',
)
