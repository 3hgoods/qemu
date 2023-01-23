

https://github.com/ljishen/Cortex-A72-Emulator
https://www.qemu.org/2018/12/12/qemu-3-1-0/



qemu-system-arm -M help | grep Cortex-A72

qemu-system-arm -M versatilepb -cpu Cortex-A72

### How to Run  (https://hub.docker.com/r/ljishen/cortex-a72-emulator )
```
git clone https://github.com/ljishen/Cortex-A72-Emulator.git
cd Cortex-A72-Emulator
docker run -ti --rm \
    --mount type=bind,src=`pwd`/images,dst=/emu \
    [-e NUM_CPUS=X] [-e CPU_CORES=X] [-e CPU_THREADS=X] [-e CPU_SOCKETS=X] \
    [-e MEMORY=X] \
    -p 5555:22 \
    ljishen/cortex-a72-emulator
 ```
