#-------------------------------------------------------------------------
#
# Makefile for src/tools/findoidjoins
#
# Copyright (c) 2003-2020, PostgreSQL Global Development Group
#
# src/tools/findoidjoins/Makefile
#
#-------------------------------------------------------------------------

subdir = src/tools/findoidjoins
top_builddir = ../../..
include $(top_builddir)/src/Makefile.global

override CPPFLAGS := -I$(libpq_srcdir) $(CPPFLAGS)
LDFLAGS_INTERNAL += $(libpq_pgport)

OBJS = \
	findoidjoins.o

all: findoidjoins

findoidjoins: findoidjoins.o | submake-libpq submake-libpgport
	$(CC) $(CFLAGS) findoidjoins.o $(LDFLAGS) $(LDFLAGS_EX) $(LIBS) -o $@$(X)

clean distclean maintainer-clean:
	rm -f findoidjoins$(X) $(OBJS)
