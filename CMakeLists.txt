cmake_minimum_required(VERSION 3.30)
project(fp_firmware C)

set(CMAKE_C_STANDARD 11)

include_directories(push)
include_directories(trunk/M880trunk)
include_directories(trunk/M880trunk/delay)
include_directories(trunk/M880trunk/face)
include_directories(trunk/M880trunk/fpsensor)
include_directories(trunk/M880trunk/iclock)
include_directories(trunk/M880trunk/modem)
include_directories(trunk/M880trunk/mp3)
include_directories(trunk/M880trunk/secu)
include_directories(trunk/M880trunk/secugen)
include_directories(trunk/M880trunk/tts)
include_directories(trunk/M880trunk/upek)
include_directories(trunk/M880trunk/webinterface)
include_directories(trunk/M880trunk/wifi)
include_directories(trunk/M880trunk/zem510)
include_directories(trunk/M880trunk/zem560)
include_directories(trunk/M880trunk/zem600)

add_executable(fp_firmware
    push/3des.c
    push/3des.h
    push/cmd.h
    push/cmd_get.c
    push/cmd_post.c
    push/data_list.c
    push/data_list.h
    push/fuliye.c
    push/fuliye.h
    push/fw_api.h
    push/http.c
    push/http.h
    push/lib.c
    push/lib.h
    push/pipe.c
    push/pipe.h
    push/pushsdk.c
    push/pushsdk.h
    push/strlist.h
    push/tcp.c
    push/tcp.h
    push/test.c
    push/thread.c
    push/thread.h
    trunk/M880trunk/delay/arca.c
    trunk/M880trunk/delay/arca.h
    trunk/M880trunk/delay/crypt.c
    trunk/M880trunk/delay/dm9000.c
    trunk/M880trunk/delay/dm9000.h
    trunk/M880trunk/delay/ezV24.c
    trunk/M880trunk/delay/ezV24.h
    trunk/M880trunk/delay/rs232comm.c
    trunk/M880trunk/delay/serial.c
    trunk/M880trunk/delay/serial.h
    trunk/M880trunk/delay/test.c
    trunk/M880trunk/delay/utils.c
    trunk/M880trunk/delay/utils.h
    trunk/M880trunk/delay/wiegand.h
    trunk/M880trunk/delay/write.c
    trunk/M880trunk/face/bmp.h
    trunk/M880trunk/face/facedb.c
    trunk/M880trunk/face/facedb.h
    trunk/M880trunk/face/facesetting.c
    trunk/M880trunk/face/ssrFaceEnroll.c
    trunk/M880trunk/face/ssrFaceInputPIN.c
    trunk/M880trunk/face/ssrFaceTest.c
    trunk/M880trunk/face/ssrFaceVerify.c
    trunk/M880trunk/face/zkface.h
    trunk/M880trunk/fpsensor/libfpsensor.h
    trunk/M880trunk/fpsensor/sensor.c
    trunk/M880trunk/fpsensor/sensor.h
    trunk/M880trunk/iclock/pushapi.c
    trunk/M880trunk/iclock/pushapi.h
    trunk/M880trunk/iclock/pushsdk_lib_api.h
    trunk/M880trunk/modem/modem.h
    trunk/M880trunk/modem/ssrmodem.c
    trunk/M880trunk/modem/ssrmodem.h
    trunk/M880trunk/mp3/audio.c
    trunk/M880trunk/mp3/audio_oss.c
    trunk/M880trunk/mp3/layer3.c
    trunk/M880trunk/mp3/mpg123.h
    trunk/M880trunk/mp3/readers.c
    trunk/M880trunk/mp3/vbrhead.c
    trunk/M880trunk/secu/arca.h
    trunk/M880trunk/secu/cim.c
    trunk/M880trunk/secu/cim.h
    trunk/M880trunk/secu/fcenter.c
    trunk/M880trunk/secu/fplib.h
    trunk/M880trunk/secu/gpio.h
    trunk/M880trunk/secu/hv7131.c
    trunk/M880trunk/secu/hv7131.h
    trunk/M880trunk/secu/io.h
    trunk/M880trunk/secu/jz_7131.c
    trunk/M880trunk/secu/kb.c
    trunk/M880trunk/secu/misc4unix.h
    trunk/M880trunk/secu/perm.h
    trunk/M880trunk/secu/secu.c
    trunk/M880trunk/secu/sensor.c
    trunk/M880trunk/secu/sensor.h
    trunk/M880trunk/secu/utype.h
    trunk/M880trunk/secu/wtype.h
    trunk/M880trunk/secugen/arca.h
    trunk/M880trunk/secugen/fcenter.c
    trunk/M880trunk/secugen/gpio.h
    trunk/M880trunk/secugen/hv7131.c
    trunk/M880trunk/secugen/hv7131.h
    trunk/M880trunk/secugen/kb.c
    trunk/M880trunk/secugen/opp03.h
    trunk/M880trunk/secugen/oppfpd.c
    trunk/M880trunk/secugen/oppfpd.h
    trunk/M880trunk/secugen/opplib.c
    trunk/M880trunk/secugen/resample.c
    trunk/M880trunk/secugen/secugen.c
    trunk/M880trunk/secugen/sensor.c
    trunk/M880trunk/secugen/sensor.h
    trunk/M880trunk/tts/tts.h
    trunk/M880trunk/tts/ttsid.h
    trunk/M880trunk/tts/ttsts.c
    trunk/M880trunk/tts/ttsts.h
    trunk/M880trunk/upek/arca.h
    trunk/M880trunk/upek/camera.c
    trunk/M880trunk/upek/cim.c
    trunk/M880trunk/upek/cim.h
    trunk/M880trunk/upek/config.h
    trunk/M880trunk/upek/dewarp.c
    trunk/M880trunk/upek/error.h
    trunk/M880trunk/upek/gpio.h
    trunk/M880trunk/upek/hv7131.c
    trunk/M880trunk/upek/hv7131.h
    trunk/M880trunk/upek/kb.c
    trunk/M880trunk/upek/linux.h
    trunk/M880trunk/upek/ov7660.h
    trunk/M880trunk/upek/sensor.c
    trunk/M880trunk/upek/sensor.h
    trunk/M880trunk/upek/upek.c
    trunk/M880trunk/upek/upek.h
    trunk/M880trunk/webinterface/webfirmware.h
    trunk/M880trunk/webinterface/webinterface.h
    trunk/M880trunk/wifi/interface.c
    trunk/M880trunk/wifi/interface.h
    trunk/M880trunk/wifi/iwlib.c
    trunk/M880trunk/wifi/iwlib.h
    trunk/M880trunk/wifi/iwlist.c
    trunk/M880trunk/wifi/newwireless.c
    trunk/M880trunk/wifi/newwireless.h
    trunk/M880trunk/wifi/ssrnewwifisetting.c
    trunk/M880trunk/wifi/ssrwifi.c
    trunk/M880trunk/wifi/ssrwifiinfo.c
    trunk/M880trunk/wifi/ssrwifiip.c
    trunk/M880trunk/wifi/ssrwifipwd.c
    trunk/M880trunk/wifi/ssrwireless.c
    trunk/M880trunk/wifi/ssrwireless.h
    trunk/M880trunk/wifi/wireless.h
    trunk/M880trunk/zem510/arca.h
    trunk/M880trunk/zem510/fcenter.c
    trunk/M880trunk/zem510/gpio.h
    trunk/M880trunk/zem510/kb.c
    trunk/M880trunk/zem510/zem510.c
    trunk/M880trunk/zem560/arca.h
    trunk/M880trunk/zem560/fcenter.c
    trunk/M880trunk/zem560/gpio.h
    trunk/M880trunk/zem560/kb.c
    trunk/M880trunk/zem560/nand.c
    trunk/M880trunk/zem560/zem560.c
    trunk/M880trunk/zem600/arca.h
    trunk/M880trunk/zem600/fcenter.c
    trunk/M880trunk/zem600/gpio.c
    trunk/M880trunk/zem600/gpio.h
    trunk/M880trunk/zem600/kb.c
    trunk/M880trunk/zem600/zem600.c
    trunk/M880trunk/alarmmng.c
    trunk/M880trunk/arabjoin.c
    trunk/M880trunk/arabjoin.h
    trunk/M880trunk/backup_restore.c
    trunk/M880trunk/backup_restore.h
    trunk/M880trunk/base64.c
    trunk/M880trunk/bidi.c
    trunk/M880trunk/camerafun.c
    trunk/M880trunk/camerafun.h
    trunk/M880trunk/capturedownload.c
    trunk/M880trunk/ccc.h
    trunk/M880trunk/clock.c
    trunk/M880trunk/commu.c
    trunk/M880trunk/commu.h
    trunk/M880trunk/convert.c
    trunk/M880trunk/convert.h
    trunk/M880trunk/convertbmp.c
    trunk/M880trunk/convertbmp.h
    trunk/M880trunk/datamap.c
    trunk/M880trunk/datamap.h
    trunk/M880trunk/delattpic.c
    trunk/M880trunk/delattpic.h
    trunk/M880trunk/DelUserWindow.c
    trunk/M880trunk/Des.c
    trunk/M880trunk/Des.h
    trunk/M880trunk/exfun.c
    trunk/M880trunk/exfun.h
    trunk/M880trunk/exfunio.h
    trunk/M880trunk/FindUserWindow.c
    trunk/M880trunk/finger.c
    trunk/M880trunk/finger.h
    trunk/M880trunk/flash.c
    trunk/M880trunk/flash.h
    trunk/M880trunk/flashdb.c
    trunk/M880trunk/flashdb.h
    trunk/M880trunk/flashdb2.c
    trunk/M880trunk/flashdb2.h
    trunk/M880trunk/fpreader.c
    trunk/M880trunk/fpreader.h
    trunk/M880trunk/Fpwindow.c
    trunk/M880trunk/getmac.c
    trunk/M880trunk/gridview.c
    trunk/M880trunk/gsm.c
    trunk/M880trunk/hid_iclass.c
    trunk/M880trunk/hid_iclass.h
    trunk/M880trunk/iclsrw.c
    trunk/M880trunk/iclsrw.h
    trunk/M880trunk/kb.h
    trunk/M880trunk/knl.h
    trunk/M880trunk/langres.h
    trunk/M880trunk/libcam.h
    trunk/M880trunk/libdlcl.h
    trunk/M880trunk/libusbdpfp.h
    trunk/M880trunk/libzklanguage.h
    trunk/M880trunk/locale.h
    trunk/M880trunk/lock.c
    trunk/M880trunk/lock.h
    trunk/M880trunk/logoneuserquery.c
    trunk/M880trunk/logquery.c
    trunk/M880trunk/lzoconf.h
    trunk/M880trunk/main.c
    trunk/M880trunk/main.h
    trunk/M880trunk/MFCardmng.c
    trunk/M880trunk/MFCardwin.c
    trunk/M880trunk/minilzo.c
    trunk/M880trunk/minilzo.h
    trunk/M880trunk/mixer.c
    trunk/M880trunk/msg.c
    trunk/M880trunk/msg.h
    trunk/M880trunk/net.c
    trunk/M880trunk/net.h
    trunk/M880trunk/netspeed.c
    trunk/M880trunk/netspeed.h
    trunk/M880trunk/number2.c
    trunk/M880trunk/options.c
    trunk/M880trunk/options.h
    trunk/M880trunk/PwdVerifyWindow.c
    trunk/M880trunk/PwdWindow.c
    trunk/M880trunk/rdm-mifare.c
    trunk/M880trunk/rdm-mifare.h
    trunk/M880trunk/RFCardwin.c
    trunk/M880trunk/risfpwindow.c
    trunk/M880trunk/rs.c
    trunk/M880trunk/rs.h
    trunk/M880trunk/rs232comm.c
    trunk/M880trunk/rs232comm.h
    trunk/M880trunk/rs_485reader.c
    trunk/M880trunk/rs_485reader.h
    trunk/M880trunk/rtc.c
    trunk/M880trunk/rtc.h
    trunk/M880trunk/serial.c
    trunk/M880trunk/serial.h
    trunk/M880trunk/SetLogqueryWindow.c
    trunk/M880trunk/SetPhotoQuery.c
    trunk/M880trunk/showmainstate.c
    trunk/M880trunk/shttpd.h
    trunk/M880trunk/srbfun.c
    trunk/M880trunk/srbfun.h
    trunk/M880trunk/ssracc.c
    trunk/M880trunk/ssracc.h
    trunk/M880trunk/ssralarm.c
    trunk/M880trunk/ssrattphotomng.c
    trunk/M880trunk/ssrauto.c
    trunk/M880trunk/ssrauto.h
    trunk/M880trunk/ssrbellmng.c
    trunk/M880trunk/ssrcard.c
    trunk/M880trunk/ssrcgroupmng.c
    trunk/M880trunk/ssrcomm.h
    trunk/M880trunk/ssrcomm1.h
    trunk/M880trunk/ssrcomm2.h
    trunk/M880trunk/ssrcomm3.h
    trunk/M880trunk/ssrcommon.c
    trunk/M880trunk/ssrcommon.h
    trunk/M880trunk/ssrdata.h
    trunk/M880trunk/ssrdatadlg.h
    trunk/M880trunk/ssrdatadown.c
    trunk/M880trunk/ssrdatapic.h
    trunk/M880trunk/ssrdataup.c
    trunk/M880trunk/ssrdate.h
    trunk/M880trunk/ssrdoor.c
    trunk/M880trunk/ssrdoormng.c
    trunk/M880trunk/ssrduressFp.c
    trunk/M880trunk/ssrduressmng.c
    trunk/M880trunk/ssrgroup.c
    trunk/M880trunk/ssrgroupmng.c
    trunk/M880trunk/ssrhday.c
    trunk/M880trunk/ssrhdaymng.c
    trunk/M880trunk/ssrhook.h
    trunk/M880trunk/ssrinfo.c
    trunk/M880trunk/ssrinfo.h
    trunk/M880trunk/ssrkeytest.h
    trunk/M880trunk/ssrlockgroup.c
    trunk/M880trunk/ssrmain.h
    trunk/M880trunk/ssrmenu.c
    trunk/M880trunk/ssrmenu.h
    trunk/M880trunk/ssrmodeminfo.c
    trunk/M880trunk/ssrmodemmng.c
    trunk/M880trunk/ssrother.c
    trunk/M880trunk/ssrpub.h
    trunk/M880trunk/ssrrecord.c
    trunk/M880trunk/ssrrestore.c
    trunk/M880trunk/ssrrtctest.h
    trunk/M880trunk/ssrsms.c
    trunk/M880trunk/ssrsmsmng.c
    trunk/M880trunk/ssrsmssend.c
    trunk/M880trunk/ssrsmsshow.c
    trunk/M880trunk/ssrsndtest.h
    trunk/M880trunk/ssrsortest.h
    trunk/M880trunk/ssrstkey.c
    trunk/M880trunk/ssrstkeymng.c
    trunk/M880trunk/ssrsystem.h
    trunk/M880trunk/ssrsystem1.c
    trunk/M880trunk/ssrsystem2.c
    trunk/M880trunk/ssrsystem2.h
    trunk/M880trunk/ssrsystem2pic.c
    trunk/M880trunk/ssrsystem2pic.h
    trunk/M880trunk/ssrsystem3.c
    trunk/M880trunk/ssrsystem4.c
    trunk/M880trunk/ssrsystem4.h
    trunk/M880trunk/ssrsystem5.h
    trunk/M880trunk/ssrsystem6.c
    trunk/M880trunk/ssrtfttest.c
    trunk/M880trunk/ssrtimezone.c
    trunk/M880trunk/ssruploadphoto.c
    trunk/M880trunk/ssruser.h
    trunk/M880trunk/ssruserlockmng.c
    trunk/M880trunk/ssrvfwin.c
    trunk/M880trunk/ssrvideoadjust.c
    trunk/M880trunk/ssrviewphoto.c
    trunk/M880trunk/ssrweb.c
    trunk/M880trunk/ssrwiegand.c
    trunk/M880trunk/ssrwiegandin.c
    trunk/M880trunk/ssrwiegandout.c
    trunk/M880trunk/ssrwkcd.c
    trunk/M880trunk/ssrwkcdmng.c
    trunk/M880trunk/strlist.c
    trunk/M880trunk/strlist.h
    trunk/M880trunk/strutils.c
    trunk/M880trunk/strutils.h
    trunk/M880trunk/t9.c
    trunk/M880trunk/t9.h
    trunk/M880trunk/t9mb.h
    trunk/M880trunk/tcpcomm.c
    trunk/M880trunk/tcpcomm.h
    trunk/M880trunk/tempdb.c
    trunk/M880trunk/tempdb.h
    trunk/M880trunk/tftlocale.c
    trunk/M880trunk/tftmsgbox.c
    trunk/M880trunk/tftmsgbox.h
    trunk/M880trunk/thread.c
    trunk/M880trunk/thread.h
    trunk/M880trunk/time.c
    trunk/M880trunk/traceroute.h
    trunk/M880trunk/truncdate.c
    trunk/M880trunk/truncdate.h
    trunk/M880trunk/updateoptions.c
    trunk/M880trunk/updatepic.c
    trunk/M880trunk/updatepic.h
    trunk/M880trunk/usb_helper.c
    trunk/M880trunk/usb_helper.h
    trunk/M880trunk/usbdpfp.h
    trunk/M880trunk/usermng.c
    trunk/M880trunk/utils.c
    trunk/M880trunk/utils.h
    trunk/M880trunk/utils2.c
    trunk/M880trunk/utils2.h
    trunk/M880trunk/VerifyModeWindow.c
    trunk/M880trunk/wav.c
    trunk/M880trunk/wav.h
    trunk/M880trunk/wiegand.c
    trunk/M880trunk/wiegand.h
    trunk/M880trunk/wiegandcode.c
    trunk/M880trunk/wiegandcode.h
    trunk/M880trunk/wireless.h
    trunk/M880trunk/writelcd.c
    trunk/M880trunk/zk_chineseLng.c
    trunk/M880trunk/zk_chineseLng.h
    trunk/M880trunk/zkfp.h
    trunk/M880trunk/zlg500b.c
    trunk/M880trunk/zlg500b.h)
