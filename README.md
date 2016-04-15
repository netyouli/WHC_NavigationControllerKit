# WHC_BannerKit

#### 联系QQ: 712641411
#### 开发作者: 吴海超
#### iOS技术交流群: 302157745
#### 轻量级的本地以及网络自动轮播器(简单，高效)

#### 最强大自动布局开源库：https://github.com/netyouli/WHC_AutoLayoutKit


### 使用效果
![](https://github.com/netyouli/WHC_BannerKit/blob/master/show.gif)

```objective-c
_banner = [[WHC_Banner alloc] initWithFrame:CGRectMake(0, 64, CGRectGetWidth([UIScreen mainScreen].bounds), bannerHeight)];
_banner.imageWidth = CGRectGetWidth([UIScreen mainScreen].bounds) / 2;
_banner.images = @[@"banner-2.jpg",@"banner-1.jpg",@"banner-0.jpg"];
_banner.pageIndicatorTintColor = [UIColor redColor];
_banner.currentPageIndicatorTintColor = [UIColor greenColor];
[self.view addSubview:_banner];
[_banner startBanner];


/// 轮播网络图片方式

// _banner4.imageUrls = @[@"http://....image.png",@"http://....image.png",@"http://....image.png",@"http://....image.png"];
/*
    _banner4.delegate = self;
- (void)WHC_Banner:(WHC_Banner *)banner networkLoadingWithImageView:(UIImageView *)imageView
          imageUrl:(NSString *)url
             index:(NSInteger)index {
// 这里加载网络图片操作 以YYWebImage为例
//[imageView yy_setImageWithURL:[NSURL URLWithString:url] placeholder:[UIImage imageNamed:@"default.png"]];
}

*/

// 或者下面方式

/*
[_banner4 setNetworkLoadingImageBlock:^(UIImageView *imageView, NSString *url, NSInteger index) {
// 这里加载网络图片操作 以YYWebImage为例
//[imageView yy_setImageWithURL:[NSURL URLWithString:url] placeholder:[UIImage imageNamed:@"default.png"]];
}];
*/

// [_banner4 startBanner];
```

