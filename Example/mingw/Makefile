TARGET = SBIClient.exe
CC = g++

#CFLAGS = -I../inc -O1 -Wall -fmessage-length=0 -finput-charset=cp932
CFLAGS = -I../inc -I../iib -O1 -Wall -fmessage-length=0

CPPFLAGS = -c

LDFLAGS = -Wl,--subsystem,console
LDLIBS = -lcomctl32 -lcomdlg32 -luser32 -lgdi32 -lkernel32 -limm32 -lwinmm -lwininet
OBJECTS = ../main.o

$(TARGET): $(OBJECTS)
		$(CC) $(CFLAGS) $(LDFLAGS) $^ $(LDLIBS) -o $@ -L../../mingw -lsbiclient

clean:
		$(RM) $(OBJECTS)
		$(RM) $(TARGET)

.c.o:
		$(CC) $(CFLAGS) $(CPPFLAGS) $< -o $@

.cpp.o:
		$(CC) $(CFLAGS) $(CPPFLAGS) $< -o $@
