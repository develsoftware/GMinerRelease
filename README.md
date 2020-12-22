# GMiner

GMiner was created by a Russian group of specialists in the field of high performance computing and cryptography.<br/>
The first version of GMiner was released on September 21, 2018 and was received quite warmly among users.<br/>
Thanks to its unique developments and stability, in just six months, the miner became a favorite on the Equihash algorithms.<br/>
The miner is focused on NVIDIA and AMD platforms and supports most popular algorithms such as: Ethash, ProgPoW, KAWPOW, Equihash, CuckooCycle.<br/>
GMiner maintains a leading position in the mining of such coins as Beam, Grin, Cortex, Bitcoin Gold.<br/>
In 2020, the miner added support for Ethash, ProgPoW and KAWPOW algorithms with high performance relative to competitors.<br/>
The development team never stops at what has been achieved and achieves the maximum performance of the algorithms with the minimum power consumption, it is these qualities that distinguish GMiner from the competitors and win the hearts of users.<br/>

# Miner Features:
+ commission is charged continuously, and not in intervals (as in most miners), which has a positive effect on the user's profitability on PPLNS pools
+ verifying generated DAG, warning when GPU overclocking is very high for Ethash, Etcash, KAWPOW and ProgPoW algorithms, helps to overclock GPU without errors
+ verifying Shares on processor, warning when GPU overclocking is very high for Ethash, Etcash, KAWPOW and ProgPoW algorithms, helps to overclock GPU without errors
+ DAG caching if the GPU has enough memory, DAG files are not recomputed when switching to another algorithm when mining Ethash + Zilliqa or Nicehash, which has a positive effect on user profitability
+ temperature control and stop the GPU in case of overheating
+ watchdog - process-observer of state of main systems of the miner, which will restart the miner in case of crash or freeze
+ mechanism to restore lost connection with pool
+ supporting failover pools, the miner uses failover pools until the connection with the main pool is restored
+ support secure connections, server certificate check (optional)
+ informative and readable tabular statistics output to console
+ display of detailed information on each device (temperature, power consumption, cooler load, memory frequency, processor frequency, energy efficiency)
+ parallel output of information to console and to file on disk
+ built-in statistics server - remote monitoring of the miner in browser

# Miner options:
'--algo' or shortly '-a' - mining algorithm ('equihash96_5', 'equihash144_5', 'equihash150_5', 'equihash192_7', 'equihash210_9', 'cuckaroo29', 'cuckatoo31', 'cuckoo' or shortly: '96_5', '144_5', '150_5', '192_7', '210_9', 'grin29', 'grin31', 'aeternity')<br/>
'--list_devices' - list devices available for mining<br/>
'--server' or shortly '-s' - mining pool address (for example: 'eu.btgpool.pro', 'eu1.zhash.pro')<br/>
'--port' or shortly '-n' - mining pool port (for example: '5057', '1445')<br/>
'--user' or shortly '-u' - mining pool login or wallet address, worker's name can be specified with a dot (for example: 'sRuJK1BmA758GbOn.worker', 'GfGLyfP9GzZbPeTzvW1KSx3HeMnrNAiGWY.rig0')<br/>
'--pass' or shortly '-p' - worker password or default pool password, can be empty, default value is 'x' (for example: 'sRuJK1Bm')<br/>
'--ssl' - enable/disable secure connection with mining pool, must be supported by a pool, can be empty, default value is '0' ('0' - off or '1' - on)<br/>
'--ssl_verification' - enable/disable certificates verification for secure connection, it may not work with pools that have expired certificate, can be empty, default value is '0' ('0' - off or '1' - on)<br/>
'--proto' - specify stratum protocol mode, possible values: proxy and stratum, useful for Ethash mining, can be empty, default value is 'proxy' (for example: 'stratum')<br/>
'--devices' or shortly '-d' - space-separated list of cuda devices, can be empty, default value is all available devices (for example: '1 3 5')<br/>
'--logfile' or shortly '-l' - filename to save logs on disk, can be empty, default value is '' (for example: '/usr/user/miner.log', 'c:\miner.log')<br/>
'--templimit' or shortly '-t' - space-separated list of temperature limits, upon reaching the limit, the GPU stops mining until it cools down, can be empty (for example: '85 80 75')
'--color' or shortly '-c' - enable/disable color output for console, default value is '1' ('0' - off or '1' - on)<br/>
'--watchdog' or shortly '-w' - enable/disable watchdog, watchdog monitors the main mining processes and restarts the application in the event of a failure or loss of connection to the pools, can be empty, default value is '1' ('0' - off or '1' - on)<br/>
'--api' - telemetry server port, allows you to monitor the miner status remotely, open a link in your browser http://localhost:<port> (for example: '10050', '20030')<br/>
'--config' - specify configuration file<br/>
'--pers' - personalization string for equihash algorithm (for example: 'BgoldPoW', 'BitcoinZ', 'Safecoin')<br/>
'--pec' - enable/disable power efficiency calculator. Power efficiency calculator display of energy efficiency statistics of GPU, higher CPU load. Default value is '1' ('0' - off or '1' - on)<br/>
'--electricity_cost' - pass cost of electricity in USD per kWh, miner will report $ spent to mining<br/>
'--intensity' or shortly '-i' - space-separated list of intensities (1-100), default value is '100' (for example: '90 90 90')<br/>
'--cache_dag' -  enable/disable caching of DAG file for mining Ethash + Zilliqa or Nicehash, default value is '1' ('0' - off or '1' - on)<br/>
'--share_check' -  enable/disable share check on CPU for mining Ethash, Etcash, KAWPOW and ProgPoW, default value is '1' ('0' - off or '1' - on)<br/>
'--nvml arg' - enable/disable NVML (statistic library for CUDA devices), default value is '1' ('0' - off or '1' - on)<br/>
'--cuda arg' - enable/disable CUDA platform, default value is '1' ('0' - off or '1' - on)<br/>
'--opencl arg' - enable/disable OpenCL platform, default value is '1' ('0' - off or '1' - on)<br/>

# Fast start:

To start Ethash, enter at the command line:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1```
--algo - mining algorithm, in this case ethash
--server - pool address and port, in this case the pool is eth.2miners.com, port is 2020
--user - Ethash wallet and worker name, in this case wallet is 0x5218597d48333d4a70cce91e810007b37e2937b5, worker is worker1

For Ethash and Etсhash algorithms, there are 2 options for stratum protocol (proxy and stratum), to explicitly specify the protocol use the "--proto" parameter, for example, to use Nicehash pool, enter in the command line:
```miner --algo ethash --server daggerhashimoto.usa.nicehash.com:3353 --user 3LsTTSsSy17xuoShcMHuRgGBxKn1AHgeVN --proto stratum```

If you have a mixed rig, you can run the miner only on CUDA devices:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --opencl 0```
or only on OpenCL devices:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --cuda 0```
or on devices of your choice, such as GPU0 GPU2 and GPU4:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --devices 0 2 4```
the list of available GPUs can be seen by calling the following command:
```miner --list_devices```

To set temperature limits on GPU0 GPU2 and GPU4, upon reaching which mining on this device will pause until it cools down:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --devices 0 2 4 --templimit 80 70 65```
where 80 is the temperature limit for GPU0, 70 is the temperature limit for GPU2, 65 is the temperature limit for GPU4

To save the miner's logs to a file for later analysis:
```miner --algo ethash --server eth.2miners.com:2020 --user 0x5218597d48333d4a70cce91e810007b37e2937b5.worker1 --logfile c: \ log.txt```
where "c:\log.txt" is the path to the file with the miner's logs

| Supported algorithms | developer commission |
|-|-|
| eth, ethash | 0.65% |
| etc, etchash | 0.65% |
| kawpow, rvn, ravencoin | 1% |
| cuckatoo32, grin32 | 2%|
| cortex | 5% |
| beamhash | 2% |
| equihash144_5 |    2%|
| equihash125_4 |    2%|
| equihash192_7 | 2% |
| equihash210_9 | 2% |
| cuckoo29, aeternity | 2%|
| cuckarood29 | 2% |
| cuckarooz29, grin29 | 3% |
| cuckatoo31, grin31 | 2%|
| cuckaroo29b, bittube | 4%|
| cuckaroo29s, swap | 2% |
| cuckarood29v, monerov | 10% |
| bfc | 3% |
| sero | 2% |
| vprogpow, vbk, veriblock | 2% |
| progpowz, zano | 2% |
| vds | 2% |
