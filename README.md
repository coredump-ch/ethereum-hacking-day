# Ethereum Hacking Day

We played around with Ethereum in the coredump hackerspace and these are our finding.

## Download the Etereum Client

### ArchLinux

On ArchLinux install geth:

```
$ sudo pacman -S geth
```

Then install mist from [AUR](https://aur.archlinux.org/packages/mist/):

```
$ yaourt -S mist
```

### Mac OSX

```
$ brew tap ethereum/ethereum
$ brew cask install ethereum
```

## Start the Testnet

There are issues with the GUI-Clients. So I suggest to use the following to get started fast \(about 15min\).

```
$ geth --fast --testnet
```

## Learning Solidity

[https://solidity.readthedocs.io/en/develop/solidity-by-example.html](https://solidity.readthedocs.io/en/develop/solidity-by-example.html)

[https://ethereum.github.io/browser-solidity/](https://ethereum.github.io/browser-solidity/)

