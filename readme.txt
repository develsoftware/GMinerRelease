Options:

'--algo' or shortly '-a' - mining algorithm ('equihash96_5', 'equihash144_5', 'equihash150_5', 'equihash192_7', 'equihash210_9', 'cuckaroo29', 'cuckatoo31', 'cuckoo' or shortly: '96_5', '144_5', '150_5', '192_7', '210_9', 'grin29', 'grin31', 'aeternity')
'--cuda_devices' - list devices available for mining
'--server' or shortly '-s' - mining pool address (for example: 'eu.btgpool.pro', 'eu1.zhash.pro')
'--port' or shortly '-n' - mining pool port (for example: '5057', '1445')
'--user' or shortly '-u' - mining pool worker name or wallet address (for example: 'sRuJK1BmA758GbOn.worker', 'GfGLyfP9GzZbPeTzvW1KSx3HeMnrNAiGWY.rig0')
'--pass' or shortly '-p' - worker password or default pool password, can be empty, default value is 'x' (for example: 'sRuJK1Bm')
'--ssl' - enable/disable secure connection with mining pool, must be supported by a pool, can be empty, default value is '0' ('0' - off or '1' - on)
'--ssl_verification' - enable/disable certificates verification for secure connection, it may not work with pools that have expired certificate, can be empty, default value is '0' ('0' - off or '1' - on)
'--devices' or shortly '-d' - space-separated list of cuda devices, can be empty, default value is all available devices (for example: '1 3 5')
'--logfile' or shortly '-l' - filename to save logs on disk, can be empty, default value is '' (for example: '/usr/user/miner.log', 'c:\miner.log')
'--templimit' or shortly '-t' - space-separated list of temperature limits, upon reaching the limit, the GPU stops mining until it cools down, can be empty (for example: '85 80 75')
'--color' or shortly '-c' - enable/disable color output for console, default value is '1' ('0' - off or '1' - on)
'--watchdog' or shortly '-w' - enable/disable watchdog, watchdog monitors the main mining processes and restarts the application in the event of a failure or loss of connection to the pools, can be empty, default value is '1' ('0' - off or '1' - on)
'--api' - telemetry server port, allows you to monitor the miner status remotely, open a link in your browser http://localhost:<port> (for example: '10050', '20030')
'--config' - specify configuration file
'--pers' - personalization string for equihash algorithm (for example: 'BgoldPoW', 'BitcoinZ', 'Safecoin')
'--pec' - enable/disable power efficiency calculator. Power efficiency calculator display of energy efficiency statistics of GPU in S/w, higher CPU load. Default value is '1' ('0' - off or '1' - on)
'--electricity_cost' - pass cost of electricity in USD per kWh, miner will report $ spent to mining

DevFee:
Fee is 2%
