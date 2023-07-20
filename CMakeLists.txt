#
# Copyright (c) 2023 Christian Spielberger
#

include(CheckIncludeFile)

zephyr_library()

zephyr_include_directories(
        ${ZEPHYR_CURRENT_MODULE_DIR}/lib/include
        ${ZEPHYR_CURRENT_MODULE_DIR}/lib/src
)

zephyr_library_compile_definitions(
   -DSTATIC
   -DSHARE_PATH="/tmp"
)

zephyr_library_sources(
  lib/src/account.c
  lib/src/aucodec.c
  lib/src/audio.c
  lib/src/aufilt.c
  lib/src/auplay.c
  lib/src/ausrc.c
  lib/src/baresip.c
  lib/src/bundle.c
  lib/src/call.c
  lib/src/cmd.c
  lib/src/conf.c
  lib/src/config.c
  lib/src/contact.c
  lib/src/custom_hdrs.c
  lib/src/descr.c
  lib/src/dial_number.c
  lib/src/event.c
  lib/src/http.c
  lib/src/log.c
  lib/src/mediadev.c
  lib/src/mediatrack.c
  lib/src/menc.c
  lib/src/message.c
  lib/src/metric.c
  lib/src/mnat.c
  lib/src/module.c
  lib/src/net.c
  lib/src/peerconn.c
  lib/src/play.c
  lib/src/reg.c
  lib/src/rtpstat.c
  lib/src/sdp.c
  lib/src/sipreq.c
  lib/src/stream.c
  lib/src/stunuri.c
  lib/src/timestamp.c
  lib/src/ua.c
  lib/src/uag.c
  lib/src/ui.c
  lib/src/vidcodec.c
  lib/src/video.c
  lib/src/vidfilt.c
  lib/src/vidisp.c
  lib/src/vidsrc.c
  lib/src/vidutil.c

  lib/modules/auconv/auconv.c
  lib/modules/auresamp/auresamp.c
  lib/modules/g711/g711.c
  lib/modules/menu/menu.c
  lib/modules/menu/dynamic_menu.c
  lib/modules/menu/static_menu.c
)
