---
layout: post
title: "Conversion of date to string and time zone"
date: 2013-12-31 17:07:05 +0800
comments: true
categories: iOS
---
    
    
今天要做個簡單個功能，將拿到的Date String轉換為當地時區。明明以前就做過了，但一直找不到過去的筆記..趁機會重寫一次。


將 `2013-12-31T02:40:34+0000` 轉換為當地格式並顯示為 `2013/12/31 10:40:34` 作法如下：

    NSDateFormatter *formatter = [[NSDateFormatter alloc] init];
    formatter.timeZone = [NSTimeZone systemTimeZone];
    formatter.dateFormat = @"yyyy-MM-dd'T'HH:mm:ssZ";
    NSDate *utcDate = [formatter dateFromString:@"2013-12-31T02:40:34+0000"];
    
    [formatter setDateFormat:@"yyyy/MM/dd HH:mm:ss"];
    NSString *localDateString = [formatter stringFromDate:utcDate];
    
以上，簡單做個記錄。