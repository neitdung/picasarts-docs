# BTFS

BitTorrent File System (BTFS) is a next-generation file sharing protocol in the BitTorrent ecosystem.

You can read full documentation of BTFS [here](https://docs.btfs.io/). In this document I just show you how to install and run BTFS node quickly on Testnet and minium system required (Mainnet will be easier, you don't need to add any flag on your commands):

- Download btfs-binary-releases file from [BTFS github releases page](https://github.com/bittorrent/go-btfs/releases)
- After download, change binary file to btfs
- Init btfs (I use command on Linux, on Windows you need change to ./btfs.exe):

     ```./btfs init --profile=storage-client-testnet``` 
- Run BTFS daemon:

     ```./btfs daemon```
- After run daemon, you can see BTTC address, ```Ctrl C``` and go to [faucet page](https://testfaucet.bt.io/) and get token to this address.
- Re-run BTFS daemon and now you can interact with this node.