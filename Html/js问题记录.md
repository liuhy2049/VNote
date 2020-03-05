# js问题记录

## 打印问题
    问题描述：IE下H5页面打印时，打印预览不显示边框
    问题原因：存在rowspan合并引起，具体原理未知
    解决方案：<!DOCTYPE html>替换为<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
