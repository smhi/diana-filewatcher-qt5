bin_PROGRAMS = filewatcher

qt_sources = \
	CoConsole.cc \
	CoFileWatcher.cc \
	CoFileWatcherThread.cc



qt_headers = $(qt_sources:.cc=.h)

nodist_filewatcher_SOURCES = $(qt_sources:.cc=_moc.cc)

filewatcher_SOURCES =   \
	main.cc       \
	$(qt_headers) \
	$(qt_sources)

AM_CPPFLAGS = -W -Wall -O2 -g -fPIC -DNOLOG4CXX
AM_LDFLAGS  = -fPIC
AM_CPPFLAGS += $(PC_CPPFLAGS)
AM_LDFLAGS  += $(PC_LDFLAGS)
LDADD       = $(PC_LIBS)


# This lets GNU make create any moc_*.cpp from the equivalent *.h
%_moc.cc: %.h
	$(MOC4) $< -o $@
