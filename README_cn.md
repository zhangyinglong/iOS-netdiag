# Network Diagnosis for iOS

[![@qiniu on weibo](http://img.shields.io/badge/weibo-%40qiniutek-blue.svg)](http://weibo.com/qiniutek)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](LICENSE.md)
[![Build Status](https://travis-ci.org/qiniu/iOS-netdiag.svg?branch=master)](https://travis-ci.org/qiniu/iOS-netdiag)
[![Latest Stable Version](http://img.shields.io/cocoapods/v/QNNetDiag.svg)](https://github.com/qiniu/iOS-netdiag/releases)
![Platform](http://img.shields.io/cocoapods/p/QNNetDiag.svg)

## 用途

网络诊断库，支持Ping/TcpPing/Rtmp/TraceRoute/DNS/外部IP/外部DNS。

## 安装

通过CocoaPods

```ruby
pod "QNNetDiag"
```

## 使用方法
### Ping
```
@interface YourLogger : NSObject <QNNOutputDelegate>
...
@end

[QNNPing start:@"www.google.com" output:[[YourLogger alloc] init] complete:^(QNNPingResult* r) {
        ...
}];
```

### TcpPing
```
[QNNTcpPing start:@"www.baidu.com" output:[[QNNTestLogger alloc] init] complete:^(QNNTcpPingResult* r) {
    ...
}];
```
## 测试


### 所有测试

``` bash
$ xctool -workspace NetDiag.xcworkspace -scheme NetDiagTests build test -sdk iphonesimulator
```

### 指定测试

可以在单元测试上修改，熟悉使用

``` bash
```

## 常见问题

- 如果碰到其他编译错误，请参考 Cocoapods 的 [troubleshooting](http://guides.cocoapods.org/using/troubleshooting.html)

## 代码贡献

详情参考[代码提交指南](https://github.com/qiniu/iOS-netdiag/blob/master/CONTRIBUTING.md)。

## 贡献记录

- [所有贡献者](https://github.com/qiniu/iOS-netdiag/contributors)

## 联系我们

- 如果有什么问题，可以到问答社区提问，[问答社区](http://qiniu.segmentfault.com/)
- 如果发现了bug， 欢迎提交 [issue](https://github.com/qiniu/iOS-netdiag/issues)
- 如果有功能需求，欢迎提交 [issue](https://github.com/qiniu/iOS-netdiag/issues)
- 如果要提交代码，欢迎提交 pull request
- 欢迎关注我们的[微信](http://www.qiniu.com/#weixin) [微博](http://weibo.com/qiniutek)，及时获取动态信息。

## 代码许可

The MIT License (MIT).详情见 [License文件](https://github.com/qiniu/iOS-netdiag/blob/master/LICENSE).
