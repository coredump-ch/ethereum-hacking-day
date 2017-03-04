# Creating Your Private Ethereum Chain

[https://www.ethereum.org/cli\#connecting-to-a-private-test-net](https://www.ethereum.org/cli#connecting-to-a-private-test-net)

https://github.com/chafey/ethereum-private-network

## Creating the Genesis Block

You don't actually need to do this, if you use  https://github.com/chafey/ethereum-private-network.

[https://blog.ethereum.org/2015/07/27/final-steps/](https://blog.ethereum.org/2015/07/27/final-steps/)

```
curl -O https://raw.githubusercontent.com/ethereum/genesis_block_generator/master/mk_genesis_block.py
```

Create a virtualenv and install the bitcoin package

```
mkvirtualenv --python=python2 ether_genesis -a $PWD
pip install bitcoin==1.1.35
```

Execute the script with the given hash \([https://twitter.com/DeathRowDemo/status/627572730699722752](https://www.gitbook.com/book/coredump-ch/ethereum-hacking-day/edit#\)\)

```
python mk_genesis_block.py  --extra-data  0x11bbe8db4e347b4e8c937c1c8370e4b5ed33adb3db69cbdb7a38e1e50b1b82fa  > genesis_block.json
```

If you get the following error:

```
API not returning data. Retrying
API not returning data. Retrying
API not returning data. Retrying
API not returning data. Retrying
Traceback (most recent call last):
  File "mk_genesis_block.py", line 293, in <module>
    print json.dumps(evaluate(), indent=4)
  File "mk_genesis_block.py", line 285, in evaluate
    p = list_purchases(th)
  File "mk_genesis_block.py", line 224, in list_purchases
    t = get_block_timestamp([x['height'] - 1 for x in subpq])
  File "mk_genesis_block.py", line 153, in new_method
    c[str(arg)] = method(arg)
```

you probably hit a rate limit of a bitcoin server. Just wait a few minutes and try again.

