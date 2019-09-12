include ../../common/make.config

LOCAL_CC = gcc -g -O3 -Wall
CC := $(CUDA_DIR)/bin/nvcc

NVCCFLAGS = -L$(CUDA_LIB_DIR) \
			 --cudart=shared
EXE = nn.out
SRC = nn_cuda.cu

all : nn hurricane_gen

clean :
	rm -rf *.o $(EXE) hurricane_gen.out

nn : nn_cuda.cu
	$(CC) -cuda $(SRC) $(NVCCFLAGS)
	$(CC) -o $(EXE) $(SRC) $(NVCCFLAGS)

clang: $(SRC)
	clang++ $(SRC) -o $(EXE)) -I../util \
		-L/usr/local/cuda/lib64 -lcudart_static -ldl -lrt -pthread -DTIMING

hurricane_gen : hurricane_gen.c
	$(LOCAL_CC) -o hurricane_gen.out $< -lm

#data :
#	mkdir data
#	./gen_dataset.sh
