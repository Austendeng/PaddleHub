# PaddleHub

[![Build Status](https://travis-ci.org/PaddlePaddle/PaddleHub.svg?branch=develop)](https://travis-ci.org/PaddlePaddle/PaddleHub)
[![License](https://img.shields.io/badge/license-Apache%202-blue.svg)](LICENSE)
[![Version](https://img.shields.io/github/release/PaddlePaddle/PaddleHub.svg)](https://github.com/PaddlePaddle/PaddleHub/releases)

PaddleHub是基于PaddlePaddle开发的预训练模型管理工具，可以借助预训练模型更便捷地开展迁移学习工作。

## 特性

通过PaddleHub，您可以：

1. 通过命令行，无需编写代码，一键使用预训练模型进行预测；
2. 通过hub download命令，快速地获取PaddlePaddle生态下的所有预训练模型；
3. 借助PaddleHub Finetune API，使用少量代码完成迁移学习；
   - 更多Demo可参考 [ERNIE文本分类](https://github.com/PaddlePaddle/PaddleHub/tree/release/v0.5.0/demo/text-classification) [图像分类迁移](https://github.com/PaddlePaddle/PaddleHub/tree/release/v0.5.0/demo/image-classification)
   - 完整教程可参考 [文本分类迁移教程](https://github.com/PaddlePaddle/PaddleHub/wiki/PaddleHub%E6%96%87%E6%9C%AC%E5%88%86%E7%B1%BB%E8%BF%81%E7%A7%BB%E6%95%99%E7%A8%8B)  [图像分类迁移教程](https://github.com/PaddlePaddle/PaddleHub/wiki/PaddleHub%E5%9B%BE%E5%83%8F%E5%88%86%E7%B1%BB%E8%BF%81%E7%A7%BB%E6%95%99%E7%A8%8B)

## 安装

**环境依赖**
* Python==2.7 or Python>=3.5
* PaddlePaddle>=1.4.0

pip安装方式如下：

```shell
$ pip install paddlehub
```

## 快速体验

安装成功后，执行下面的命令，可以快速体验PaddleHub无需代码、一键预测的命令行功能：

```shell
# 使用百度LAC词法分析工具进行分词
$ hub run lac --input_text "今天是个好日子"

# 使用百度Senta情感分析模型对句子进行预测
$ hub run senta_bilstm --input_text "今天是个好日子"

# 使用SSD检测模型对图片进行目标检测，检测结果如下图所示
$ wget --no-check-certificate https://paddlehub.bj.bcebos.com/resources/test_img_bird.jpg
$ hub run ssd_mobilenet_v1_pascal --input_path test_img_bird.jpg
```
![SSD检测结果](https://raw.githubusercontent.com/PaddlePaddle/PaddleHub/develop/docs/imgs/test_img_bird_output.jpg)

想了解更多PaddleHub已经发布的模型，请使用`hub search`命令查看所有已发布的模型。

```shell
$ hub search
```

## 深入了解PaddleHub
* [PaddleHub Wiki](https://github.com/PaddlePaddle/PaddleHub/wiki)
* [命令行工具](https://github.com/PaddlePaddle/PaddleHub/wiki/PaddleHub%E5%91%BD%E4%BB%A4%E8%A1%8C%E5%B7%A5%E5%85%B7)
* [Finetune API与迁移学习](https://github.com/PaddlePaddle/PaddleHub/wiki/PaddleHub%E4%B8%8E%E8%BF%81%E7%A7%BB%E5%AD%A6%E4%B9%A0)
* [API](https://github.com/PaddlePaddle/PaddleHub/wiki/PaddleHub-Finetune-API)

## 答疑

当安装或者使用遇到问题时，可以通过[FAQ](https://github.com/PaddlePaddle/PaddleHub/wiki/PaddleHub-FAQ)查找解决方案。
如果在FAQ中没有找到解决方案，欢迎您将问题和bug报告以[Github Issues](https://github.com/PaddlePaddle/PaddleHub/issues)的形式提交

## 版权和许可证
PaddleHub由[Apache-2.0 license](LICENSE)提供
