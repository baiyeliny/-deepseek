# DeepSeek多平台接入实现

> 全网首个多语言实现的DeepSeek API接入开源项目

作者: 白夜 (b站: 柏枼凛音)

## 项目简介

这是一个创新性的项目，提供了三种不同语言实现的DeepSeek API接入方案：
1. AGG脚本实现 (Lua + Android UI)
2. 命令行工具实现 (C语言)
3. 轻量级实现 (纯Lua)

本项目为全网首发的完整DeepSeek API接入方案，涵盖了从命令行到图形界面的多种实现方式。

## 特性

### 共同特性
- 支持多个DeepSeek模型:
  - DeepSeek-Chat V3 通用对话模型
  - DeepSeek-Reasoner R1 推理模型
- 完整的错误处理机制
- 支持API版本选择

### AGG版本特性
- 优雅的Android原生界面
- 支持回答复制、继续对话等功能
- 完整的会话管理

### C语言版本特性
- 命令行交互界面
- 支持模型和API接口动态切换
- 低资源占用
- 更适合服务器部署

### 纯Lua版本特性
- 代码精简，易于理解
- 快速部署
- 适合嵌入其他Lua项目

## 实现对比

| 特性 | AGG版本 | C语言版本 | 纯Lua版本 |
|------|---------|-----------|------------|
| UI类型 | Android原生界面 | 命令行 | 简单对话框 |
| 适用场景 | 移动设备 | 服务器/桌面 | 轻量级应用 |
| 代码复杂度 | 中等 | 较高 | 低 |
| 功能完整性 | 完整 | 完整 | 基础功能 |

## 使用方法

### AGG版本
1. 配置API密钥
2. 启动脚本
3. 选择模型并开始对话

### C语言版本
1. 编译源码：
```bash
gcc -o deepseek_chat main.c
```
2. 配置API密钥
3. 运行程序并按提示操作

### 纯Lua版本
1. 配置API密钥
2. 直接运行脚本
3. 按提示选择模型并输入问题

## 注意事项

- 使用前请确保已获取DeepSeek的API密钥
- 不同版本适用于不同场景，请根据需求选择
- AGG版本需要AGG环境支持
- C语言版本需要curl支持
- 纯Lua版本需要Lua环境支持

## 技术细节

### AGG版本
- 使用Android原生控件
- MaterialCardView界面设计
- 异步请求处理

### C语言版本
- 使用libcurl进行HTTP请求
- JSON手动解析
- 命令行参数处理

### 纯Lua版本
- 简单HTTP请求封装
- 基础JSON处理
- 精简的对话管理

## 开源协议

本项目采用MIT协议开源，欢迎贡献代码和提出建议。

## 更新日志

### v1.0.0 (首个版本)
- 实现三种不同语言的API接入
- 支持多模型选择
- 完成基础功能和界面
- 添加错误处理机制

## 贡献指南

欢迎提交Pull Request，改进代码实现或添加新功能。提交时请说明：
1. 改进的具体内容
2. 测试方法
3. 使用示例

## 致谢

- DeepSeek团队提供的API支持
- AGG平台提供的开发环境
- 社区贡献者的宝贵建议

## 联系方式

- B站：柏枼凛音
- 项目问题请提交Issue
