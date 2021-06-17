GMiner was created by a Russian group of specialists in the field of high performance computing and cryptography.
The first version of GMiner was released on September 21, 2018 and was received quite warmly among users.
Thanks to its unique developments and stability, in just six months, the miner became a favorite on the Equihash algorithms.
The miner is focused on NVIDIA and AMD platforms and supports most popular algorithms such as: Ethash, ProgPoW, KAWPOW, Equihash, CuckooCycle.
GMiner maintains a leading position in the mining of such coins as Beam, Grin, Cortex, Bitcoin Gold.
In 2020, the miner added support for Ethash, ProgPoW and KAWPOW algorithms with high performance relative to competitors.
The development team never stops at what has been achieved and achieves the maximum performance of the algorithms with the minimum power consumption, it is these qualities that distinguish GMiner from the competitors and win the hearts of users.

# Miner Features:
* commission is charged continuously, and not in intervals (as in most miners), which has a positive effect on the user's profitability on PPLNS pools
* verifying generated DAG, warning when GPU overclocking is very high for Ethash, Etcash, KAWPOW and ProgPoW algorithms, helps to overclock GPU without errors
* verifying Shares on processor, warning when GPU overclocking is very high for Ethash, Etcash, KAWPOW and ProgPoW algorithms, helps to overclock GPU without errors
* DAG caching if the GPU has enough memory, DAG files are not recomputed when switching to another algorithm when mining Ethash + Zilliqa or Nicehash, which has a positive effect on user profitability
* auto selection of optimal kernels for each device on Ethash, Etcash, KAWPOW
* ability to manually select kernel on each device for Ethash, Etcash
* temperature control and stop the GPU in case of overheating
* watchdog - process-observer of state of main systems of the miner, which will restart the miner in case of crash or freeze
* mechanism to restore lost connection with pool
* supporting failover pools, the miner uses failover pools until the connection with the main pool is restored
* support secure connections
* support SOCKS5 proxy
* informative and readable tabular statistics output to console
* display of detailed information on each device (temperature, power consumption, cooler load, memory frequency, processor frequency, energy efficiency)
* parallel output of information to console and to file on disk
* built-in statistics server - remote monitoring of the miner in browser
* memory tweaks for Nvidia GPUs with GDDR5X and GDDR5 memory
* core clocks, memory clocks, core voltage, memory voltage, fan speed, power limit overclocking for Windows
* safe DAG generation for Nvidia GPUs
* automatic fan speed control for target temperature

# Miner options:
```--algo``` or shortly ```-a``` - mining algorithm (for example: 'ethash', 'kawpow', 'cuckatoo32', 'beamhash')
```--list_devices``` - list devices available for mining
```--server``` or shortly ```-s``` - mining pool address (for example: 'eu.btgpool.pro', 'eu1.zhash.pro')
```--port``` or shortly ```-n``` - mining pool port (for example: '5057', '1445')
```--user``` or shortly ```-u``` - mining pool login or wallet address, worker's name can be specified with a dot (for example: 'sRuJK1BmA758GbOn.worker', 'GfGLyfP9GzZbPeTzvW1KSx3HeMnrNAiGWY.rig0')
```--worker``` - worker name for Ethash strarum, for pools that does not supoort wallet.worker (for example: 'rig0') 
```--pass``` or shortly ```-p``` - worker password or default pool password, default value is 'x' (for example: 'sRuJK1Bm')
```--ssl``` - enable/disable secure connection with mining pool, must be supported by a pool, default value is '0' ('0' - off or '1' - on)
```--proxy``` - SOCKS5 proxy server address (for example: 31.7.232.178:1080)
```--proto``` - specify stratum protocol mode, possible values: proxy and stratum, useful for Ethash mining, default value is 'proxy' (for example: 'stratum')
```--dag_mode``` - space-separated list of Dag file modes (0 - auto, 1 - single, 2 - double), default is '0' (for example: '2 1 0')
```--safe_dag``` - space-separated list of DAG generation modes (0 - auto, 1 - fast mode, 2 - safe mode, in auto mode GTX GPUs - fast DAG and RTX GPUs - safe DAG), only Nvidia GPUs are supported, default is '0' (for example: '2 1 0')
```--dag_limit``` - space-separated list of Dag file size limits in megabytes, to disable the limit use 0, default is '0' (for example: '4096 4096 4096')
```--cache_dag``` -  enable/disable caching of DAG file for mining Ethash + Zilliqa or Nicehash, default value is '1' ('0' - off or '1' - on)
```--devices``` or shortly ```-d``` - space-separated list of cuda devices, default value is all available devices (for example: '1 3 5')
```--kernel``` or shortly ```-k``` - space-separated list of kernel numbers for each device (0 - auto, 1-6 - kernel number, currently supports 6 kernels for Nvidia on Ethash/Etchash) (for example: '1 3 5')
```--mt``` - space-separated list of memory tweak numbers for each device (range from 0 to 6, 0 - disable tweaks), only Nvidia GPUs with GDDR5X and GDDR5 memory are supported, requires running miner with admin privileges (for example: '1 3 5')
```--fan``` - space-separated list of fan speed for each device in percents (range from 0 to 100, 0 - ignore), only Windows is supported (for example: '60 0 90')
```--pl``` - space-separated list of power limits for each device in percents (range from 0 to 100 for Nvidia GPUs and -50 - 50 for AMD GPUs, 0 - ignore), only Windows is supported (for example: '30 0 50')
```--cclock``` - space-separated list of core clock offsets (for Nvidia GPUs) or absolute core clocks (for AMD GPUs) for each device in MHz (0 - ignore), only Windows is supported, requires running miner with admin privileges (for example: '100 0 -90')
```--mclock``` - space-separated list of memory clock offsets (for Nvidia GPUs) or absolute memory clocks (for AMD GPUs) for each device in MHz (0 - ignore), only Windows is supported, requires running miner with admin privileges (for example: '100 0 -90')
```--cvddc``` - space-separated list of core voltage offsets in % (for Nvidia GPUs) or absolute core voltages (for AMD GPUs) for each device in mV (0 - ignore), only Windows is supported, requires running miner with admin privileges (for example: '900 0 1100')
```--mvddc``` - space-separated list of absolute memory voltages for each device in mV (0 - ignore), only Windows and AMD GPUs are supported, requires running miner with admin privileges (for example: '900 0 1100')
```--lock_voltage``` - space-separated list of locked voltage points for each device in mV (0 - ignore), only Windows and Nvidia GPUs are supported. Requires running miner with admin privileges (for example: '900 0 1000')
```--lock_cclock``` - space-separated list of locked core clock point for each device in MHz (0 - ignore), only Nvidia GPUs are supported. Requires running miner with admin privileges (for example: '1200 0 1500')
```--p2state``` - enable/disable P2 state, only Windows and Nvidia GPUs are supported. Requires running miner with admin privileges
```--tfan``` - space-separated list of target temperatures for fan (0 - ignore), only Windows is supported (for example: '65 0 70')
```--tfan_min``` - space-separated list of minimal fan speed (0 - ignore) for tfan option, only Windows is supported (for example: '30 0 35')
```--tfan_max``` - space-separated list of maximal fan speed (0 - ignore) for tfan option, only Windows is supported (for example: '90 0 80')
```--logfile``` or shortly ```-l``` - filename to save logs on disk, default value is '' (for example: '/usr/user/miner.log', 'c:\miner.log')
```--log_date``` - enable/disable date in each message, default value is '0' ('0' - off or '1' - on)
```--log_stratum``` - enable/disable data of communication with the server, default value is '0' ('0' - off or '1' - on)
```--log_newjob``` - enable/disable information about new jobs, default value is '1' ('0' - off or '1' - on)
```--templimit``` or shortly ```-t``` - space-separated list of temperature limits, upon reaching the limit, the GPU stops mining until it cools down (for example: '85 80 75')
```--color``` or shortly ```-c``` - enable/disable color output for console, default value is '1' ('0' - off or '1' - on)
```--watchdog``` or shortly ```-w``` - enable/disable watchdog, watchdog monitors the main mining processes and restarts the application in the event of a failure or loss of connection to the pools, default value is '1' ('0' - off or '1' - on)
```--api``` - telemetry server port, allows you to monitor the miner status remotely, open a link in your browser http://localhost:port (for example: '10050', '20030')
```--config``` - specify configuration file
```--pers``` - personalization string for equihash algorithm (for example: 'BgoldPoW', 'BitcoinZ', 'Safecoin')
```--pec``` - enable/disable power efficiency calculator. Power efficiency calculator display of energy efficiency statistics of GPU, higher CPU load. Default value is '1' ('0' - off or '1' - on)
```--electricity_cost``` - pass cost of electricity in USD per kWh, miner will report $ spent to mining
```--intensity``` or shortly ```-i``` - space-separated list of intensities (1-100), default value is '100' (for example: '90 90 90') 
```--share_check``` -  enable/disable share check on CPU for mining Ethash, Etcash, KAWPOW and ProgPoW, default value is '1' ('0' - off or '1' - on)
```--nvml``` - enable/disable NVML (statistic library for CUDA devices), default value is '1' ('0' - off or '1' - on)
```--cuda``` - enable/disable CUDA platform, default value is '1' ('0' - off or '1' - on)
```--opencl``` - enable/disable OpenCL platform, default value is '1' ('0' - off or '1' - on)
```--opencl``` - enable/disable OpenCL platform, default value is '1' ('0' - off or '1' - on)

Parameters dag_mode, safe_dag, dag_limit, kernel, mt, fan, pl, cclock, cvddc, mclock, mvddc, lock_voltage, lock_cclock, tfan, templimit, intensity can be specified with one parameter for all devices:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --kernel 0 --templimit 80 --dag_mode 0```
or for each device separately, if we have 3 devices:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --kernel 0 1 1 --templimit 80 70 90 --dag_mode 0 1 2```

Miner supports failover pools, if the main pool is not available, the miner switches to the failover pools, after the main pool is available, the miner will switch to it, example:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --server eu1.ethermine.org:4444 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --server asia.sparkpool.com:3333 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1```
eth.2miners.com - main pool
eu1.ethermine.org and asia.sparkpool.com - failover pools

Miner resets mt, cclock, cvddc, mclock, mvddc parameters to default values while DAG generation to avoid errors

# Parameters details:
```--kernel``` - allows you to choose one of several kernels, the fastest kernel is automatically selected by default. 
Cores differ in performance and energy efficiency depending on the GPU model and overclocking parameters. 
To set the kernel manually, pass the kernel index to the parameter. 
Try to choose the best kernel for you manually by going through all the options

```--mt``` - allows you to choose one of several tweaks for GPUs with GDDR5X and GDDR5 memory. 
A higher value gives more performance and less stability, risk of finding invalid shares increases. 
Try to check all values to determine which one suits you best.
Administrator rights required. 

```--safe_dag``` - allows you to choose a way to DAG generation.
In fast mode (value 1, auto for GTX GPUs) miner generates DAG as quickly as possible, DAG errors are possible at maximum overclocking.
In safe mode (value 2, auto for RTX GPUs) miner generates DAG with error control, useful for RTX cards at maximum overclocking.

```--tfan``` - allows you to set a target temperature for fans.
Miner monitors temperature of GPU and actively controls the fan speed trying to hold target temperature.
```--tfan_min``` and ```--tfan_max``` options set minimum and maximum fan speed limits.

# Fast start:
To start Ethash, enter at the command line:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1```
```--algo``` - mining algorithm, in this case ethash
```--server``` - pool address and port, in this case the pool is eth.2miners.com, port is 2020
```--user``` - Ethash wallet and worker name, in this case wallet is 0x5218597d48333d4a70cce91e810007b37e2937b5, worker is worker1

For Ethash and Etchash algorithms, there are 2 options for stratum protocol (proxy and stratum), to explicitly specify the protocol use the ```--proto``` parameter, for example, to use Nicehash pool, enter in the command line:
```miner --algo ethash --server daggerhashimoto.usa.nicehash.com:3353 --user 3LsTTSsSy17xuoShcMHuRgGBxKn1AHgeVN --proto stratum```

If you have a mixed rig, you can run the miner only on CUDA devices:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --opencl 0```
or only on OpenCL devices:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --cuda 0```
or on devices of your choice, such as GPU0 GPU2 and GPU4:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --devices 0 2 4```
the list of available GPUs can be seen by calling the following command:
```miner --list_devices```

For Ethash and Etchash algorithms there is a possibility of manual selection of kernels:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --kernel 0 2 3```
```--kernel 0 2 3``` - kernel numbers for each device, 0 - auto kernel selection for GPU0, kernel #2 for GPU1, kernel #3 for GPU2

Also you can select one kernel for all devices:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --kernel 5```
```--kernel 5``` select kernel #5 for all devices

To set temperature limits on GPU0 GPU2 and GPU4, upon reaching which mining on this device will pause until it cools down:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --devices 0 2 4 --templimit 80 70 65```
where 80 is the temperature limit for GPU0, 70 is the temperature limit for GPU2, 65 is the temperature limit for GPU4

To save the miner's logs to a file for later analysis:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --logfile c:\log.txt```
where "c:\log.txt" is the path to the file with the miner's logs

# Supported algorithms and developer commission:
|-|-|
| eth, ethash | 0.65% |
| etc, etchash | 0.65% |
| kawpow, rvn, ravencoin | 1% |
| cuckatoo32, grin32 | 2% |
| cortex | 5% |
| beamhash | 2% |
| equihash144_5 | 2% |
| equihash125_4 | 2% |
| equihash192_7 | 2% |
| equihash210_9 | 2% |
| cuckoo29, aeternity | 2% |
| cuckatoo31, grin31 | 2% |
| cuckaroo29b, bittube | 4% |
| cuckaroo29s, swap | 2% |
