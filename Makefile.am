bin_SCRIPTS = cfg/*.py cfg/*.sh

cfgdir = $(sysconfdir)/sonic
cfg_SCRIPTS = cfg/*.xml

svcdir = $(sysconfdir)/sysctl.d
svc_SCRIPTS = cfg/etc/sysctl.d/*

bin_PROGRAMS=sonic_nas_daemon

sonic_nas_daemon_SOURCES=src/main.c src/hald_init.c

sonic_nas_daemon_LIBADD= -lsonic_logging -lsonic_object_library \
                         -lpthread -lm -lsystemd  -lsonic_nas_ndi \
                         -lsonic_common -lsonic_nas_common -lsai-common \
                         -lsonic_nas_interface -lsonic_nas_platform \
                         -lsonic_hal_routing -lsonic_nas_l2 -lsonic_nas_qos \
                         -lsonic_nas_packet_io -lsonic_nas_linux -lsonic_nas_acl

sonic_nas_daemon_CPPFLAGS= -I$(top_srcdir)/sonic -I$(includedir)/sonic
systemdconfdir=/lib/systemd/system
systemdconf_DATA = cfg/*.service
