GMiner was created by a Russian group of specialists in the field of high performance computing and cryptography.<br/>
The first version of GMiner was released on September 21, 2018 and was received quite warmly among users.<br/>
Thanks to its unique developments and stability, in just six months, the miner became a favorite on the Equihash algorithms.<br/>
The miner is focused on NVIDIA and AMD platforms and supports most popular algorithms such as: Ethash, ProgPoW, KAWPOW, Equihash, CuckooCycle.<br/>
GMiner maintains a leading position in the mining of such coins as Beam, Grin, Cortex, Bitcoin Gold.<br/>
In 2020, the miner added support for Ethash, ProgPoW and KAWPOW algorithms with high performance relative to competitors.<br/>
The development team never stops at what has been achieved and achieves the maximum performance of the algorithms with the minimum power consumption, it is these qualities that distinguish GMiner from the competitors and win the hearts of users.<br/>

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
* support failover pools, the miner uses failover pools until the connection with the main pool is restored
* support secure connections
* support SOCKS5 proxy
* support tor network
* informative and readable tabular statistics output to console
* display of detailed information on each device (temperature, power consumption, cooler load, memory frequency, processor frequency, energy efficiency)
* parallel output of information to console and to file on disk
* built-in statistics server - remote monitoring of the miner in browser
* memory tweaks for Nvidia GPUs with GDDR5X and GDDR5 memory
* core clocks, memory clocks, core voltage, memory voltage, fan speed, power limit overclocking for Windows
* safe DAG generation for Nvidia GPUs
* automatic fan speed control for target temperature
* support charging of maintenance fee


# Miner options:
```--help``` or shortly ```-h``` - display available options<br/>
```--version``` or shortly ```-v``` - print program version<br/>
```--user_id``` - print user ID<br/>
```--algo``` or shortly ```-a``` - mining algorithm (for example: 'ethash', 'kawpow', 'cuckatoo32', 'beamhash')<br/>
```--list_devices``` - list devices available for mining<br/>
```--contest_wallet``` - Ethash wallet, parameter is required to participate in contest<br/>
```--server``` or shortly ```-s``` - mining pool address (for example: 'eu.btgpool.pro', 'eu1.zhash.pro')<br/>
```--port``` or shortly ```-n``` - mining pool port (for example: '5057', '1445')<br/>
```--user``` or shortly ```-u``` - mining pool login or wallet address, worker's name can be specified with a dot (for example: 'sRuJK1BmA758GbOn.worker', 'GfGLyfP9GzZbPeTzvW1KSx3HeMnrNAiGWY.rig0')<br/>
```--worker``` - worker name for Ethash strarum, for pools that does not supoort wallet.worker (for example: 'rig0') <br/>
```--pass``` or shortly ```-p``` - worker password or default pool password, default value is 'x' (for example: 'sRuJK1Bm')<br/>
```--ssl``` - enable/disable secure connection with mining pool ('0' - off or '1' - on), must be supported by a pool, default value is '0' <br/>
```--proxy``` - SOCKS5 proxy server address (for example: 31.7.232.178:1080)<br/>
```--proto``` - specify stratum protocol mode, possible values: proxy and stratum, useful for Ethash mining, default value is 'proxy' (for example: 'stratum')<br/>
```--dag_mode``` - space-separated list of Dag file modes (0 - auto, 1 - single, 2 - double), default is '0' (for example: '2 1 0')<br/>
```--safe_dag``` - space-separated list of DAG generation modes (0 - auto, 1 - fast mode, 2 - safe mode, in auto mode GTX GPUs - fast DAG and RTX GPUs - safe DAG), only Nvidia GPUs are supported, default is '0' (for example: '2 1 0')<br/>
```--dag_limit``` - space-separated list of Dag file size limits in megabytes, to disable the limit use 0, default is '0' (for example: '4096 4096 4096')<br/>
```--cache_dag``` -  enable/disable caching of DAG file for mining Ethash + Zilliqa or Nicehash('0' - off or '1' - on), default value is '1'<br/>
```--dag_gen_limit``` - maximal number of parallel DAG generations, 0 - disable limit, default value is '0' (for example: '3')<br/>
```--devices``` or shortly ```-d``` - space-separated list of cuda devices, default value is all available devices (for example: '1 3 5')<br/>
```--kernel``` or shortly ```-k``` - space-separated list of kernel numbers for each device (0 - auto, 1-6 - kernel number, currently supports 6 kernels for Nvidia on Ethash/Etchash) (for example: '1 3 5')<br/>
```--mt``` - space-separated list of memory tweak numbers for each device (range from 0 to 6, 0 - disable tweaks), only Nvidia GPUs with GDDR5X and GDDR5 memory are supported, requires running miner with admin privileges (for example: '1 3 5')<br/>
```--fan``` - space-separated list of fan speed for each device in percents (range from 0 to 100, 0 - ignore), only Windows is supported (for example: '60 0 90')<br/>
```--pl``` - space-separated list of power limits for each device in percents (range from 0 to 100 for Nvidia GPUs and -50 - 50 for AMD GPUs, 0 - ignore), only Windows is supported (for example: '30 0 50')<br/>
```--cclock``` - space-separated list of core clock offsets (for Nvidia GPUs) or absolute core clocks (for AMD GPUs) for each device in MHz (0 - ignore), only Windows is supported, requires running miner with admin privileges (for example: '100 0 -90')<br/>
```--mclock``` - space-separated list of memory clock offsets (for Nvidia GPUs) or absolute memory clocks (for AMD GPUs) for each device in MHz (0 - ignore), only Windows is supported, requires running miner with admin privileges (for example: '100 0 -90')<br/>
```--cvddc``` - space-separated list of core voltage offsets in % (for Nvidia GPUs) or absolute core voltages (for AMD GPUs) for each device in mV (0 - ignore), only Windows is supported, requires running miner with admin privileges (for example: '900 0 1100')<br/>
```--lock_voltage``` - space-separated list of locked voltage points for each device in mV (0 - ignore), only Windows and Nvidia GPUs are supported. Requires running miner with admin privileges (for example: '900 0 1000')<br/>
```--lock_cclock``` - space-separated list of locked core clock point for each device in MHz (0 - ignore), only Nvidia GPUs are supported. Requires running miner with admin privileges (for example: '1200 0 1500')<br/>
```--p2state``` - enable/disable P2 state, only Windows and Nvidia GPUs are supported. Requires running miner with admin privileges<br/>
```--tfan``` - space-separated list of target temperatures for fan (0 - ignore), only Windows is supported (for example: '65 0 70')<br/>
```--tfan_min``` - space-separated list of minimal fan speed (0 - ignore) for tfan option, only Windows is supported (for example: '30 0 35')<br/>
```--tfan_max``` - space-separated list of maximal fan speed (0 - ignore) for tfan option, only Windows is supported (for example: '90 0 80')<br/>
```--logfile``` or shortly ```-l``` - filename to save logs on disk, default value is '' (for example: '/usr/user/miner.log', 'c:\miner.log')<br/>
```--log_date``` - enable/disable date in each message, default value is '0' ('0' - off or '1' - on)<br/>
```--log_stratum``` - enable/disable data of communication with the server, default value is '0' ('0' - off or '1' - on)<br/>
```--log_newjob``` - enable/disable information about new jobs, default value is '1' ('0' - off or '1' - on)<br/>
```--templimit``` or shortly ```-t``` - space-separated list of temperature limits, upon reaching the limit, the GPU stops mining until it cools down (for example: '85 80 75')<br/>
```--templimit_mem``` or shortly ```-tm``` - space-separated list of memory temperature limits, upon reaching the limit, the GPU stops mining until it cools down (for example: '95 100 105')<br/>
```--color``` or shortly ```-c``` - enable/disable color output for console, default value is '1' ('0' - off or '1' - on)<br/>
```--watchdog``` or shortly ```-w``` - enable/disable watchdog, watchdog monitors the main mining processes and restarts the application in the event of a failure or loss of connection to the pools, default value is '1' ('0' - off or '1' - on)<br/>
```--watchdog_restart_delay``` - miner restart delay for watchdog in seconds, default value is '10' (for example: '1')<br/>
```--watchdog_mode``` - watchdog action on miner quits (0 - restart miner, 1 - reboot system), default value is '0' (for example: '1')<br/>
```--min_rig_speed``` - minimal rig speed, miner quits if average speed drop below specified value<br/>
```--report_interval``` - statistics report interval in seconds, default value is '30' (for example: '5')<br/>
```--api``` - telemetry server port, allows you to monitor the miner status remotely, open a link in your browser http://localhost:port (for example: '10050', '20030')<br/>
```--config``` - specify configuration file<br/>
```--pers``` - personalization string for equihash algorithm (for example: 'BgoldPoW', 'BitcoinZ', 'Safecoin')<br/>
```--pec``` - enable/disable power efficiency calculator. Power efficiency calculator display of energy efficiency statistics of GPU, higher CPU load. Default value is '1' ('0' - off or '1' - on)<br/>
```--electricity_cost``` - pass cost of electricity in USD per kWh, miner will report $ spent to mining<br/>
```--intensity``` or shortly ```-i``` - space-separated list of intensities (1-100), default value is '100' (for example: '90 90 90') <br/>
```--share_check``` -  enable/disable share check on CPU for mining Ethash ('0' - off or '1' - on), Etcash, KAWPOW and ProgPoW, default value is '1'<br/>
```--nvml``` - enable/disable NVML (statistic library for CUDA devices) ('0' - off or '1' - on), default value is '1'<br/>
```--cuda``` - enable/disable CUDA platform ('0' - off or '1' - on), default value is '1'<br/>
```--opencl``` - enable/disable OpenCL platform ('0' - off or '1' - on) , default value is '1'<br/>
```--lhr``` - space-separated list of LHR modes (0 - auto, 1 - on, 2 - off), only Nvidia GPUs are supported<br/>
```--lhr_tune``` - space-separated list of LHR tune values, meaning GPU unlock percentage (0 - auto), only Nvidia GPUs are supported, default value is '0' (for example: '72 71 73')<br/>
```--lhr_autotune``` - space-separated list of LHR auto-tune, 0 - off, 1 - on, only Nvidia GPUs are supported (for example: '1 0 1')<br/>
```--lhr_autotune_step``` - LHR auto-tune step size, only Nvidia GPUs are supported, default value is '0.1' (for example: '0.2')<br/>
```--lhr_mode``` - space-separated list of LHR mode (0 - power save mode, 1 - maximal performance mode), only Nvidia GPUs are supported, default value is '1' (for example: '1 0 1')<br/>
```--secure_dns``` - enable/disable only DNS over HTTPS requests<br/>
```--maintenance_server``` - mining pool address for maintenance (for example: 'eu.btgpool.pro', 'eu1.zhash.pro')<br/>
```--maintenance_port``` - mining pool port for maintenance (for example: '5057', '1445')<br/>
```--maintenance_user``` - mining pool login or wallet address for maintenance<br/>
```--maintenance_pass``` - worker password or default pool password for maintenance<br/>
```--maintenance_ssl``` - enable/disable secure connection with mining pool ('0' - off or '1' - on) for maintenance, must be supported by a pool, default value is '0' <br/>
```--maintenance_proto``` - specify stratum protocol mode for maintenance, possible values: proxy and stratum, useful for Ethash mining, default value is 'proxy' (for example: 'stratum')<br/>
```--maintenance_worker``` - worker name for Ethash strarum for maintenance, for pools that does not supoort wallet.worker (for example: 'rig0')<br/>
```--maintenance_fee``` - maintenance fee percent<br/>
```--tor``` - enable/disable network connections through Tor<br/>
```--tor_exit_node``` - space-separated list of exit node for Tor network (for example: 'en', 'fr')<br/>

Parameters dag_mode, safe_dag, dag_limit, kernel, mt, fan, pl, cclock, cvddc, mclock, lock_voltage, lock_cclock, tfan, templimit, templimit_mem, intensity, lhr, lhr_tune, lhr_autotune, lhr_mode can be specified with one parameter for all devices:<br/>
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --kernel 0 --templimit 80 --dag_mode 0```<br/>
or for each device separately, if we have 3 devices:<br/>
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --kernel 0 1 1 --templimit 80 70 90 --dag_mode 0 1 2```<br/>

Miner supports failover pools, if the main pool is not available, the miner switches to the failover pools, after the main pool is available, the miner will switch to it, example:<br/>
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --server eu1.ethermine.org:4444 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --server asia.sparkpool.com:3333 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1```<br/>
eth.2miners.com - main pool<br/>
eu1.ethermine.org and asia.sparkpool.com - failover pools<br/>

Miner supports charging of maintenance fee (maintenance fee charging after charging developers fee), example:<br/>
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --maintenance_server eth.2miners.com:2020 --maintenance_user 0x270686d8A5c33Ba2E584EF8e94128A07B57BcB2A --maintenance_fee 20```<br/>
eth.2miners.com:2020 - maintenance fee pool<br/>
0x270686d8A5c33Ba2E584EF8e94128A07B57BcB2A - maintenance fee wallet<br/>
20 - maintenance fee percent<br/>

Miner resets mt, cclock, cvddc, mclock parameters to default values while DAG generation to avoid errors<br/>

# Parameters details:
```--kernel``` - allows you to choose one of several kernels, the fastest kernel is automatically selected by default. <br/>
Cores differ in performance and energy efficiency depending on the GPU model and overclocking parameters. <br/>
To set the kernel manually, pass the kernel index to the parameter. <br/>
Try to choose the best kernel for you manually by going through all the options<br/>

```--mt``` - allows you to choose one of several tweaks for GPUs with GDDR5X and GDDR5 memory. <br/>
A higher value gives more performance and less stability, risk of finding invalid shares increases. <br/>
Try to check all values to determine which one suits you best.<br/>
Administrator rights required. <br/>

```--safe_dag``` - allows you to choose a way to DAG generation.<br/>
In fast mode (value 1, auto for GTX GPUs) miner generates DAG as quickly as possible, DAG errors are possible at maximum overclocking.<br/>
In safe mode (value 2, auto for RTX GPUs) miner generates DAG with error control, useful for RTX cards at maximum overclocking.<br/>

```--tfan``` - allows you to set a target temperature for fans.<br/>
Miner monitors temperature of GPU and actively controls the fan speed trying to hold target temperature.<br/>
```--tfan_min``` and ```--tfan_max``` options set minimum and maximum fan speed limits.<br/>

# Fast start:
To start Ethash, enter at the command line:<br/>
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1```<br/>
```--algo``` - mining algorithm, in this case ethash<br/>
```--server``` - pool address and port, in this case the pool is eth.2miners.com, port is 2020<br/>
```--user``` - Ethash wallet and worker name, in this case wallet is 0x5218597d48333d4a70cce91e810007b37e2937b5, worker is worker1<br/>

For Ethash and Etchash algorithms, there are 2 options for stratum protocol (proxy and stratum), to explicitly specify the protocol use the ```--proto``` parameter, for example, to use Nicehash pool, enter in the command line:<br/>
```miner --algo ethash --server daggerhashimoto.usa.nicehash.com:3353 --user 3LsTTSsSy17xuoShcMHuRgGBxKn1AHgeVN --proto stratum```<br/>

If you have a mixed rig, you can run the miner only on CUDA devices:<br/>
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --opencl 0```<br/>
or only on OpenCL devices:<br/>
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --cuda 0```<br/>
or on devices of your choice, such as GPU0 GPU2 and GPU4:<br/>
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --devices 0 2 4```<br/>
the list of available GPUs can be seen by calling the following command:<br/>
```miner --list_devices```<br/>

For Ethash and Etchash algorithms there is a possibility of manual selection of kernels:<br/>
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --kernel 0 2 3```<br/>
```--kernel 0 2 3``` - kernel numbers for each device, 0 - auto kernel selection for GPU0, kernel #2 for GPU1, kernel #3 for GPU2<br/>

Also you can select one kernel for all devices:<br/>
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --kernel 5```<br/>
```--kernel 5``` select kernel #5 for all devices<br/>

To set temperature limits on GPU0 GPU2 and GPU4, upon reaching which mining on this device will pause until it cools down:<br/>
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --devices 0 2 4 --templimit 80 70 65```<br/>
where 80 is the temperature limit for GPU0, 70 is the temperature limit for GPU2, 65 is the temperature limit for GPU4<br/>

To save the miner's logs to a file for later analysis:<br/>
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --logfile c:\log.txt```<br/>
where "c:\log.txt" is the path to the file with the miner's logs<br/>

# Supported algorithms and developer commission:
|algorithm|fee|
|-|-|
| eth, ethash | 2% |
| etc, etchash | 2% |
| kawpow, rvn, ravencoin | 2% |
| autolykos2, ergo | 2% |
| kheavyhash, kaspa | 1% |
| cortex | 5% |
| beamhash | 2% |
| equihash144_5 | 2% |
| equihash125_4 | 2% |
| equihash210_9 | 2% |
| cuckoo29, aeternity | 2% |

# Resources:
Official site: http://gminer.pro <br/>
Github: https://github.com/develsoftware/GMinerRelease <br/>
BitcoinTalk: https://bitcointalk.org/index.php?topic=5034735.0 <br/>
Discord: https://discord.gg/J7RUG3FDYw <br/>
Telegram chat: https://t.me/gminer_talk <br/>
Telegram announcements: https://t.me/gminer_releases <br/>
