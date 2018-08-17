## Requirements
- PHP 7.1+
- composer
- ext-gmp
- mdanter/ecc

## Dependencies
1) go to the folder with the script `crypt_example.php`
2) install  `composer require mdanter/ecc:0.5.0`
3) create the folder `data` and set permissions 0777

## Usage

```shell
php crypt_example.php [params]
```

## List of methods:


#### generate
Generate MH address

```shell
php crypt_example.php method=generate
```

#### fetch-balance
Get balance for MH address

Params:
- net - network (main, dev)
- address - MH address

```shell
php crypt_example.php method=fetch-balance net=dev address=0x003d3b27f544d1dc03d6802e6379fdcfc25e0b73272b62496b
```
#### fetch-history
Get history for MH address

Params:
- net - network (main, dev)
- address - MH address

```shell
php crypt_example.php method=fetch-history net=dev address=0x003d3b27f544d1dc03d6802e6379fdcfc25e0b73272b62496b
```

#### get-tx
Get transaction information by hash

Params:
- net - network (main, dev)
- hash - transaction hash

```shell
php crypt_example.php method=get-tx net=dev hash=ee0e11b793ff5a5b0d6954f0da4964ceb53f9887480e9a5e42608830ed401963
```

#### send-tx
Create and send transaction

Params:
- net - network (main, dev)
- address - MH address (from created addresses)
- to - MH address
- value

```shell
php crypt_example.php method=send-tx net=dev address=0x003d3b27f544d1dc03d6802e6379fdcfc25e0b73272b62496b to=0x00525d3f6326549b8974ef669f8fced6153109ba60d52d547d value=1000 
```