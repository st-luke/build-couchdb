## Process this file with automake to create Makefile.in

## Copyright (C) 2001, 2002 Free Software Foundation, Inc.
##
## This program is free software; you can redistribute it and/or modify
## it under the terms of the GNU General Public License as published by
## the Free Software Foundation; either version 2, or (at your option)
## any later version.
##
## This program is distributed in the hope that it will be useful,
## but WITHOUT ANY WARRANTY; without even the implied warranty of
## MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
## GNU General Public License for more details.
##
## You should have received a copy of the GNU General Public License
## along with this program; if not, write to the Free Software
## Foundation, Inc., 59 Temple Place - Suite 330, Boston, MA
## 02111-1307, USA.

autoconflibdir = $(pkgdatadir)/autoconf
dist_autoconflib_DATA = \
	autoconf.m4 \
	general.m4 status.m4 oldnames.m4 specific.m4 \
	autoheader.m4 autoupdate.m4 autotest.m4 autoscan.m4 \
	lang.m4 c.m4 fortran.m4 \
	functions.m4 headers.m4 types.m4 libs.m4 programs.m4

nodist_autoconflib_DATA = autoconf.m4f
CLEANFILES = $(nodist_autoconflib_DATA)


## --------------- ##
## Building TAGS.  ##
## --------------- ##

TAGS_FILES = $(dist_autoconflib_DATA)

ETAGS_ARGS = $(ETAGS_FOR_AUTOCONF)


## -------- ##
## Checks.  ##
## -------- ##

check-local: check-forbidden-patterns
forbidden_patterns = -e '^_*EOF' -e ' cmp '
forbidden_patterns_files = $(dist_autoconflib_DATA)


## ------------------ ##
## The frozen files.  ##
## ------------------ ##

autoconf.m4f: $(autoconf_m4f_dependencies)
include ../freeze.mk
