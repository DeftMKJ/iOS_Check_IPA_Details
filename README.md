# iOS_Check_IPA_Details

## 该脚本为了在Python3x上用，把原先2.7版本的脚本做了修改[2.7版本](https://github.com/apperian/iOS-checkIPA)

`listipa.py` 扫描获取IPA文件并解析其Info.plist（在Payload目录中）和embedded.mobileprovision文件

## Installation ##
正常情况下，把`listipa.py`文件去掉后缀名，然后把整个文件丢进`/usr/local/bin`里面，就可以直接在终端使用了，但是现在默认是2.x的Python版本，所以这里不建议这么用，但是老版本是可以这么操作的

## Usage ##
1.下载
```shell
git clone git@github.com:DeftMKJ/iOS_Check_IPA_Details.git
```
2.`cd`到项目
```shell
cd /Users/mikejing191/Downloads/iOS_Check_IPA_Details-master
```
3.查看使用方式
```shell
python3 listipa.py --help

Usage: listipa.py [options]

Options:
  --version             show program's version number and exit
  -h, --help            show this help message and exit
  -i INPUT_FILE, --ipafile=INPUT_FILE
                        provide IPA filename
  -u UDIDS, --udids=UDIDS
                        check if udids are provisioned
  -v, --verbose         print data structures to stdout
```

4.使用Python3调用  `python3 listipa.py -i xxx.ipa`
```shell
python3 listipa.py -i /Users/mikejing191/Desktop/SmartPay_Example-IPA/SmartPay_Example-v1.4.1-b20190703142838.ipa

```

5.Log
```shell
 IPA File Integrity: "SmartPay_Example-v1.4.1-b20190703142838.ipa"
    =================================================================
    
    Info
    ----
      Name: SmartPay_Example
      Version: 20190703142838
      Expiration Date: 2020-06-16 05:45:26
      Distribution Profile Type: Ad Hoc/Developer
      Provisioned Devices (50): 
      22bc9e335a458ecdd1bac6c9f91a974d78d080e0
      00008020-000335413612002E
      c07800eeeb9e2882ba5fdc8056ba068e52a13972
      74fb2c4f32623f7de25ecabbf3e818863a1cb383
      56a144828e02a3910ab98341aa0a8097a15df032
      882bef326581e6c6243892afcaf75663c569c526
      c36dd5cd4bcf659ecc883f8b102c9adc14021676
      15d6fa010b32100e7ba65524347ead9157528b37
      67c33f00c76b7d8994c25bff8255ae3e6514a673
      0c1b07a820edc7d2dceae4bf0863a1cdf9066a02
      f71956f0879a656df87015803b280e2519c37b81
      a4212f2e9991bee7b1b138a970a9bf25dc15bbd3
      e5ff6dc7eb7ae52ac4b84017d37046838b4c5d0d
      790d27ed999d3de1ce146fa677adfb22c79c2aad
      5d3f14c5edb424b9720f32b1e84490436ba8ffd0
      beed94ee1dc88ed3b3ce8bf246d0d3f37195482f
      00008020-0019441E0A7A002E
      14e5207eac76ea722bf97595ac1f868615cef8e5
      b5c14a2c8114d81487f6bb7e4197ac44b21b978d
      c2bca9348e4b34f1b73e4f8fdeebcf06250a9fbd
      c2e759296f219d1e1610a6c3f47bc46ddfd90423
      1ac5518a9dd9a27a68f7e52e3459a71c0b973c2b
      33f8f8d54231b94aad4ac494d2a9f2598a2830d8
      aa30d2f9ff6ad0d258ab66940c9828d9c65cdf13
      a3abc21d85bf9d48fb217aaef0ffc8a98852f0ee
      a532ca7e977d785c636b57bb6b908e2eea5d866c
      63b6735bcb993e1274f9dd77e7e97b991a0842a1
      b4a3de621822e3453f2910d79206fcfd80234a39
      5ff73f510801014953ca83c03ec76ae49c4822c1
      675c8a7f9211943ffd44716fd36a145be96bae4e
      8158bdfa6177e694d0f5a5b0e370c7d735d5018b
      01742fbad591135c2cbbb1ab41bc6bc37d24af48
      2367e1ef32c61ab766e4d62677b09150f498cf0a
      86c76e054ba7847f80e92649cdbaa4370018dd28
      e2c9ae4451084d9c4df4e93e87c7f85961d97109
      508679ecc7c5da22a72143485f5bc779f2c31e8e
      0ab8a74f62177bfce52fd6d94d04871ce24153a9
      f0c4750abd50dc4ee4d99635a32ddfeed81699ab
      1841391aa60d110b06a05b1e7682f1764727834f
      00008020-000651AA2EF8002E
      4e1d43cae2172b7da63d534b7d5f0ba60b96f12a
      d098c7bc47a69f10e4de8d4136228db070c4dd1c
      00008020-00012C6A1A84002E
      69e8cee91197b44f63f14de6f07ba8cb7b5737a5
      f0fe2f461e0ea5384ef974a16f9e3b785f8ce3de
      0690fa06dc6a850dc5a06d27ffebba9db3a2291f
      00008020-001949843690003A
      cf325a61d28acb65bcf8eca1ff4e8d25e548c0a6
      7fabdd02245932c86f807f3413c4cdf012ea5a10
      00008020-00013044016A002E
    
    Warnings
    --------
      Push Notification: not enabled
      Push Notification: aps-environment key is not set
      Distribution: code signing Entitlements 'get-task-allow' value is set to YES; should be NO
    
    Errors
    ------
      none


```
