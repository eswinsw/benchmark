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
|CoreMark-PRO|EEMBC CoreMark-PRO. Five prevalent integer workloads and four popular floating-point workloads.|
