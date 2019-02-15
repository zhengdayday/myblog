---
title: flutter学习
date: 2019-02-01 09:56:43
categories:
- Flutter
tags: 
- 教程
thumbnail: /img/one主题/康娜.gif
primarycolor: brown
accentcolor: blueGrey
---
    
### 包与代码说明
    
1. [*包结构和各个service层保持一致,目录位于web模块下面src/main/test/java*]
2. [*类名和service保持一致, 并且继承BaseJunit*]
(如: ReportServiceImpl-\> ReportServiceImplTest extends BaseJunit)
3. [*方法名和service的方法名称保持*]
4. [*使用@Autowired导入需要进行测试的类,然后在对应的测试方法中调用该类的方法*]
5. [*代码编写:例子*]

```java
public class CourtAnnouncementFilterServiceImplTest extends BaseJunit {
        
            @Autowired
            private CourtAnnouncementFilterService courtAnnouncementFilterService;
        
            @Test
            public void getLegalAnnouncement() throws IOException {
                CourtAnnouncementFilterActionRequest actionRequest = new CourtAnnouncementFilterActionRequest(
                        "小米科技有限责任公司",
                        "",
                        "",
                        1,
                        20,
                        1
                );
                Optional<AnnouncementFilterDetailMapper> legalAnnouncement = courtAnnouncementFilterService.getLegalAnnouncement(actionRequest);
                legalAnnouncement.map(BasicMapper::getData).ifPresent(BaseJunit::toJson);
            }
        }
```
####执行方法
`mvn test`

注:如果需要跳过测试需要加上`-Dmaven.test.skip=true`命令

     
     