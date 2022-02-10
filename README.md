```--secure_dns``` - enable/disable only DNS over HTTPS requests<br/>
```--maintenance_server``` - mining pool address for maintenance (for example: 'eu.btgpool.pro', 'eu1.zhash.pro')<br/>
```--maintenance_port``` - mining pool port for maintenance (for example: '5057', '1445')<br/>
```--maintenance_user``` - mining pool login or wallet address for maintenance<br/>
```--maintenance_pass``` - worker password or default pool password for maintenance<br/>
```--maintenance_ssl``` - enable/disable secure connection with mining pool ('0' - off or '1' - on) for maintenance, must be supported by a pool, default value is '0' <br/>
```--maintenance_proto``` - specify stratum protocol mode for maintenance, possible values: proxy and stratum, useful for Ethash mining, default value is 'proxy' (for example: 'stratum')<br/>
```--maintenance_worker``` - worker name for Ethash strarum for maintenance, for pools that does not supoort wallet.worker (for example: 'rig0')<br/>
```--maintenance_fee``` - maintenance fee percent<br/>

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
| eth, ethash | 1% |
| etc, etchash | 1% |
| kawpow, rvn, ravencoin | 1% |
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
