
PATH_PRU_SW=../../am335x_pru_package/pru_sw/
PATH_PRU_LOADER=$(PATH_PRU_SW)app_loader/

CFLAGS=-Wall -I$(PATH_PRU_LOADER)include -I/usr/include/python3.2 -shared -fPIC
LDFLAGS=-Llib -lprussdrv -lpthread -fPIC
OBJ=pypruss.o
TARGET=../../pypruss.so

.PHONY: clean all

all: $(TARGET)

$(OBJ): $(OBJ:%.o=%.c)
	gcc $(CFLAGS) -c -o $@ $< 

$(TARGET): $(OBJ)
	gcc $(CFLAGS) -o $@ $^ $(LDFLAGS)


clean: 
	rm -rf $(OBJ) *~ $(TARGET)



