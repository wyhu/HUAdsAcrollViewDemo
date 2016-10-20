# HUAdsAcrollViewDemo
轮播图（支持自动滑动，支持手动滑动，自定义界面）
***

##使用方法

```
    NSURL *url = [NSURL URLWithString:@"http://img4.bbs.szhome.com/UploadFiles/Images/2009/06/30/0630154313327.jpg"];
    
    //图片（支持image,NSUrl,NSString）
    NSArray *imgArr = [NSArray arrayWithObjects:@"http://img4.bbs.szhome.com/UploadFiles/Images/2009/06/30/0630154313327.jpg",[UIImage imageNamed:@"屏幕快照 2016-10-20 下午2.04.12"],url, nil];
    //标题
    NSArray *titleArr = [NSArray arrayWithObjects:@"第一个",@"第二个",@"第三个", nil];
    
    HUAdsScrollView *ads =  [[HUAdsScrollView alloc] initWithFrame:CGRectMake(0, 100, self.view.bounds.size.width, 250) imgArr:imgArr titleArr:titleArr];
    
    //滑动时间间隔
    ads.changeTime = 3.0;
    
    //回调事件
    [ads setBlock:^(NSInteger currPage) {
        
        NSLog(@"%ld",currPage);
    }];
    
    [self.view addSubview:ads];

```
