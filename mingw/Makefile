TARGET = sbiclient.dll
CC = g++

CFLAGS = -I..\\src -O1 -Wall -fmessage-length=0 -shared
CPPFLAGS = -c

LDFLAGS =
LDLIBS = -lcomctl32 -lcomdlg32 -luser32 -lgdi32 -lkernel32 -limm32 -lwinmm -lwininet

OBJECTS = \
          ..\\src\\CBufferString.o  \
          ..\\src\\CDate.o		    \
          ..\\src\\CHtmlTokenizer.o \
          ..\\src\\CHttpClient.o	\
          ..\\src\\CSBIWebClient.o  \
          ..\\Dll\\SBIClient.o      \
          ..\\Dll\\dllmain.o \

$(TARGET): $(OBJECTS)
		$(CC) $(CFLAGS) $(LDFLAGS) $^ $(LDLIBS) -o $@

clean:
		$(RM) $(OBJECTS)
		$(RM) $(TARGET)

.c.o:
		$(CC) $(CFLAGS) $(CPPFLAGS) $< -o $@

.cpp.o:
		$(CC) $(CFLAGS) $(CPPFLAGS) $< -o $@
