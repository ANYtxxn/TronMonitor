# TRON Transfer Script Usage Guide

## Introduction

This script is designed to monitor a TRON wallet's balance and automatically transfer funds to designated addresses when the balance exceeds a specified threshold.

## Configuration File

Create a `config.json` file with the following fields:

- `api_list`: List of TRON node APIs
- `from_address`: The TRON wallet address to monitor
- `to_addresses`: List of destination addresses to receive transfers
- `private_keys`: List of private keys for signing transactions
- `permission_id`: Permission ID required to broadcast transactions (default is 2)
- `funds_threshold`: Balance threshold to trigger transfers (in TRX)

## Running the Script

1. Place `config.json` in the same directory as the executable.
2. Run the executable.

## How it Works

1. Loads the configuration from `config.json`.
2. Tests nodes in `api_list` to find available nodes.
3. Checks if `funds_threshold` is valid.
4. Continuously monitors the balance of `from_address`.
5. Initiates a transfer when the balance exceeds `funds_threshold`:
   - Checks available bandwidth.
   - Calculates transfer amount based on bandwidth.
   - Randomly selects a destination address from `to_addresses`.
   - Signs the transaction using `private_keys`.
   - Broadcasts the transaction to the TRON network.
6. Waits 3 seconds and repeats the monitoring.

## Application Scenarios

- **AUTOMATIC TRANSFER**: Use this script to transfer TRX after taking profits, eliminating the need for manual transfers.
- **Fund Management**: In multi-signature wallet scenarios, this script can automatically transfer excess funds to other addresses to help manage them.


----



# TRON转账脚本使用指南

## 介绍

该脚本旨在监控TRON钱包的余额， 当余额超过设定的阈值时，自动将资金转移到指定地址。

## 配置文件

创建一个名为 `config.json` 的配置文件，包含以下字段：

- `api_list`: TRON节点API列表
- `from_address`: 要监控的TRON钱包地址
- `to_addresses`: 用于接收转账的目标地址列表
- `private_keys`: 用于签名交易的私钥列表
- `permission_id`: 广播交易所需的权限ID (默认为2)
- `funds_threshold`: 触发转账的余额阈值 (TRX)

## 运行脚本

1. 将 `config.json` 文件放置在与可执行文件相同的目录中。
2. 运行可执行文件。

## 脚本执行流程

1. 从 `config.json` 加载配置。
2. 测试 `api_list` 中的节点以查找可用节点。
3. 检查 `funds_threshold` 是否有效。
4. 持续监控 `from_address` 的余额。
5. 当余额超过 `funds_threshold` 时进行转账：
   - 检查可用带宽。
   - 根据带宽计算转账金额。
   - 从 `to_addresses` 随机选择一个目标地址。
   - 使用 `private_keys` 对交易进行签名。
   - 将交易广播到 TRON 网络。
6. 等待 3 秒并重复监控。

## 应用场景

- **自动转移**: 使用该脚本在获利后转账TRX，免除手动转账。
- **资金管理**: 在多签名钱包场景中，该脚本可以自动将多余资金转账到其他地址来帮助管理。

## 高级版本
当前脚本为免费试用版本
联系**TG@chidafen @tronluke**获取付费版本
#### 付费功能
1. 自定义TRC20通证转账(USDT等)
2. 多地址同时监控
3. 更完善的监控机制
4. 更多附加功能定制

