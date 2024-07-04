# What does hybrid mean?

We took the best parts from the GPU and CPU miner and combined them resulting in massive gains in performance and efficiency.

Examples from our testers:
7970X + 4090
- Individual Performance: 250 + 250 it/s
- Combined performance: 950 + 90 it/s

7950X + 4070 ti
- Individual Performance: 140 + 70 it/s
- Combined performance: 500 + 45 it/s

# How to run

First download the correct binary from the releases in this repo.
Similar to the regular CPU miner you will have to set the amount of threads as well as a payout ID and an optional label. For the GPU part of this implementation an additional parameter is required that sets the amount of resources used by your GPU(s).

`rqiner -t <threads> -i <payout-id> -l <label> -n <ndatasets>`

The -n parameter has to be a single value or a comma seperated list e.g.
`-n 500 300 500`
If you set 3 values for n they will be mapped to GPU 0, 1, 2 respectively. Ideal values for n are somewhere between 100-600 depending on your GPU, e.g. 4090: n=500, 4070ti: n=250. In order to find the optimal configuration you can run the GPU miner which will tell you the amount of blocks used in its optimal configuration after the auto-tuning is finished, which you can input as value for your -n parameter.

## Discord

For further help with setting up the miner you can join our official Discord server

[![](https://img.shields.io/discord/1179806757204267090?color=5865F2&logo=Discord&style=flat-square)](https://discord.gg/zTrdShyQu2)
