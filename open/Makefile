
TARGET = otest

CC = cc
CFLAGS = -Wall -Wextra -O2 -g
LDFLAGS = -llfapi
LINCLUDE = ../../lfapi

SRCS = opentest.c
OBJS = $(SRCS:.c=.o)
DEPS = $(SRCS:.c=.d)

all: $(TARGET)

$(TARGET): $(OBJS)
	$(CC) -L$(LINCLUDE) -o $@ $^ $(LDFLAGS)

$(OBJS): $(SRCS)
	$(CC) $(CFLAGS) -MMD -c $< -o $@

-include $(DEPS)

clean:
	rm -rf $(TARGET_O) $(OBJS) $(DEPS)


