# benchmark

A benchmarking suite script for RISC-V.

## Usage

    ./run_benchmark.sh -l|--list
    ./run_benchmark.sh [options] <benchmark>
        -h, --help        show this help
        -l, --list        list all supported benchmarks
        --from-source     compile from source instead of using distro's version

## Suite

|Benchmark Name|Description|
|---|---|
|zstd| A fast lossless compression algorithm from Facebook.|
|ffmpeg| Audio/Video encoding performance with ffmpeg.|
|numpy| Uses NumPy official benchmark suite to test the performance of NumPy.|
|openssl| Measures the RSA 4096-bit performance of OpenSSL.|
|povray| POV-Ray, the Persistence of Vision Raytracer. POV-Ray is used to create 3D graphics using ray-tracing.|
|m-queens| A solver for the N-queens problem with multi-threading support via the OpenMP library. For benchmarking the OpenMP performance.|
|lmbench|A suite of simple, portable, ANSI/C microbenchmarks for UNIX/POSIX, measures latency and bandwidth.|
|ebizzy|A program to generate workloads resembling web server workloads.|
|iperf| Network performance benchmark for kernel and NIC.|
|CorMark|CoreMark's primary goals are simplicity and providing a method for testing only a processor's core features.|
|CoreMark-sifive|Sifive maintains its own version of the CoreMark benchmark. It produces higher scores than the official CoreMark.|
|CoreMark-PRO|EEMBC CoreMark-PRO. Five prevalent integer workloads and four popular floating-point workloads.|
|embench|A suite of free and open source C benchmarks for embedded systems|
|glmark2|OpenGL 2.0 and ES 2.0 benchmark|


## Notes

### Compiling sifive coremark on ARM platforns
When compliing for 64bit with

```
$ make PORT_DIR=linux64
```

The resulting binary produces some error messages. It can be fixed by making the following changes in linux64/core_portme.h

```
/* typedef unsigned long long ee_ptr_int; */
typedef ee_u32 ee_ptr_int;
```
