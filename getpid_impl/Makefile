CFLAGS := -Wall -Wextra -O3 -D'uint64_t=unsigned long'
MEM    := 4

all: ex1

ex1: pid_example.c
	../selfie -c pid_example.c -o pid_example.m

run_ex1: ex1
	../selfie -l pid_example.m -m $(MEM)

run_ex1_on_selfie: ex1
	../selfie -c ../selfie.c -m 64 -l pid_example.m -m $(MEM)

run_all: run_ex1

run_all_on_selfie: run_ex1_on_selfie

clean:
	@rm -f *.m