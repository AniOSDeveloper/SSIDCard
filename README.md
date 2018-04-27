# SSIDCard

[![Version](https://img.shields.io/cocoapods/v/SSIDCard.svg?style=flat)](https://cocoapods.org/pods/SSIDCard)
[![License](https://img.shields.io/cocoapods/l/SSIDCard.svg?style=flat)](https://cocoapods.org/pods/SSIDCard)
[![Platform](https://img.shields.io/cocoapods/p/SSIDCard.svg?style=flat)](https://cocoapods.org/pods/SSIDCard)
![图片](http://oarzzvu0u.bkt.clouddn.com/idcard.gif)

## 介绍
扫描识别身份证号，完美支持bitcode。上图是直接扫描搜索的照片，所以没有打码😊

## 使用
- info.plist文件中增加`Privacy - Camera Usage Description`描述，否则崩溃
- 导入头文件`<SSIDCard/SSIDCard.h>`
- 两种调用方式：
	- block:
	```ruby
	SSScanViewController *scanVC = [[SSScanViewController alloc] 
	initWithBlock:^(NSString *result) {
		NSLog(@"%@", result);
	}];
	```
	- delegate
	```
	- (void)ss_scanViewController:(SSScanViewController *)scanViewController
   didObtainedRecognizeResult:(NSString *)recognizeResult {
	NSLog(@"%@", recognizeResult);;
}
	```

## Author

sansansisi, zhangjiamingcoder@gmail.com

## License

SSIDCard is available under the MIT license. See the LICENSE file for more info.
