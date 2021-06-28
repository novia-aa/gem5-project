# gem5-project

1.GEM5 + NVMAIN BUILD-UP !
Follow tuitor

2.Enable L3 last level cache in GEM5 + NVMAIN !


3.Config last level cache to  2-way and full-way associative cache and test performance !
2-way code

<code>
 
./build/X86/gem5.opt configs/example/se.py -c tests/test-progs/hello/bin/x86/linux/quicksort --cpu-type=TimingSimpleCPU --caches --l2cache --l3cache --l1i_size=32kB --l1d_size=32kB --l2_size=128kB --l3_size=1MB --l3_assoc=2 --mem-type=NVMainMemory --nvmain-config=../NVmain/Config/PCM_ISSCC_2012_4GB.config

</code>

full-way code

<code>
 
./build/X86/gem5.opt configs/example/se.py -c tests/test-progs/hello/bin/x86/linux/quicksort --cpu-type=TimingSimpleCPU --caches --l2cache --l3cache --l1i_size=32kB --l1d_size=32kB --l2_size=128kB --l3_size=1MB --l3_assoc=16384 --mem-type=NVMainMemory --nvmain-config=../NVmain/Config/PCM_ISSCC_2012_4GB.config

</code>


4.Modify last level cache policy based on RRIP !
add replacement_policy in L3 cache


5.Test the performance of write back and write through policy based on 4-way associative cache with isscc_pcm!
