#
# $Id: Makefile,v 1.4 2002/03/27 02:36:28 bbraun Exp $
#
# This Makefile controls a build process of $(TITLE) module for
# Linux-PAM. You should not modify this Makefile (unless you know
# what you are doing!).
#

include ../../Make.Rules

TITLE=pam_limits

ifeq ($(OS),linux)

LOCAL_CONFILE=./limits.skel
INSTALLED_CONFILE=$(SCONFIGD)/limits.conf

DEFS=-DDEFAULT_CONF_FILE=\"$(INSTALLED_CONFILE)\"
CFLAGS += $(DEFS)

MODULE_SIMPLE_INSTALL=bash -f ../install_conf "$(FAKEROOT)" "$(SCONFIGD)" "$(INSTALLED_CONFILE)" "$(TITLE)" "$(LOCAL_CONFILE)"
MODULE_SIMPLE_REMOVE=rm -f $(FAKEROOT)$(INSTALLED_CONFILE)
MODULE_SIMPLE_CLEAN=rm -f ./.ignore_age

include ../Simple.Rules

else

include ../dont_makefile

endif
