SOURCES = kernel.s

%.o: %.s
	ca65 --cpu 6502 -o $@ -l $(@:.o=.lst) $<

all: kernel

kernel: $(SOURCES:.s=.o)
	cl65 --cpu 6502 -C kernel.cfg -t none -o $@ $^

clean:
	rm -f kernel *.o *.lst
