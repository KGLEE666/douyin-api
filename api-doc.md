> 抖音API文档

**<a href='#login'>0.api登录（获取token</a><br>**
**<a href='#refresh'>1.刷新token</a><br>**
**<a href='#account_list'>2.账号列表</a><br>**
**<a href='#account_detail'>3.账号详情</a><br>**
**<a href='#video_list'>4.账号视频列表</a><br>**
**<a href='#video_detail'>5.视频详情</a><br>**
**<a href='#musics'>6.账号音乐列表</a><br>**
**<a href='#music_videos'>7.音乐视频列表</a><br>**
**<a href='#hot_search'>8.抖音热搜榜</a><br>**
**<a href='#hot_video'>9.今日最热视频</a><br>**
**<a href='#hot_music'>10.DOU听音乐榜</a><br>**
**<a href='#followings'>11.关注列表</a><br>**
**<a href='#followers'>12.粉丝列表</a><br>**
**<a href='#comments'>13.评论列表</a><br>**
**<a href='#feeds'>14.feeds</a><br>**
**<a href='#challengets'>15.挑战列表</a><br>**
**<a href='#challenget_detail'>16.挑战详情</a><br>**
**<a href='#challenget_videos'>17.挑战视频列表</a><br>**
**<a href='#sticker_info'>18.贴纸详情</a><br>**
**<a href='#sticker_videos'>19.贴纸视频列表</a><br>**
**<a href='#favorite'>20.收藏列表</a><br>**
**<a href='#nearby'>21.附近人</a><br>**
**<a href='#poi_detail'>22.定位信息</a><br>**
**<a href='#poi_videos'>23.定位信息视频列表</a><br>**
**<a href='#live_list'>24.直播列表</a><br>**
**<a href='#live_rank'>25.直播礼物榜</a><br>**
**<a href='#live_promotions'>26.直播购物车</a><br>**
**<a href='#promotions'>27.橱窗商品列表</a><br>**
**<a href='#product'>28.商品详情</a><br>**
**<a href='#order_share'>29.商品晒单列表</a><br>**
**<a href='#product_comments'>30.商品评价列表</a><br>**

----

**<span id='login'>0.api登录</span>**

`url`：`{host}/api/auth/open_api_login`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | mobile | 电话号码 | Y |  |
| 2 | password | 密码 | Y |  |

返回数据示例

```
{
    "code": 1,
    "data": {
        "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC9sb2NhbC5hcGkudmlkZW9yYW5rLmNuXC9hcGlcL2F1dGhcL2xvZ2luIiwiaWF0IjoxNTU4OTQ5NjIxLCJleHAiOjE1OTA0ODU2MjEsIm5iZiI6MTU1ODk0OTYyMSwianRpIjoib1djTWx5WVFPNzNTNG95SyIsInN1YiI6MSwicHJ2IjoiMjNiZDVjODk0OWY2MDBhZGIzOWU3MDFjNDAwODcyZGI3YTU5NzZmNyJ9.OzxU3JqY23CmnUx7bI38WyTR6oe11UURXwKxRWySGAA",
        "token_type": "bearer",
        "expires_in": 60
    },
    "message": "登录成功"
}
```

**<span id='refresh'>1.刷新</a>token**

*注：需要在`headers`中传递`token`
`url`：`{host}/api/open/auth/refresh`

返回参数示例：

```
{
    "code": 1,
    "data": {
        "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC9sb2NhbC5hcGkudmlkZW9yYW5rLmNuXC9hcGlcL2F1dGhcL3JlZnJlc2giLCJpYXQiOjE1NTg3OTI4MDAsImV4cCI6MTU5MDU2MDQxMCwibmJmIjoxNTU5MDI0NDEwLCJqdGkiOiJOUlZMWmxKUnpkMHJYSllRIiwic3ViIjoxLCJwcnYiOiIyM2JkNWM4OTQ5ZjYwMGFkYjM5ZTcwMWM0MDA4NzJkYjdhNTk3NmY3In0.Cd5Ryy_MRu0CWVf_hSMBtbZn9mHn92elDZcn5qSpl6A",
        "token_type": "bearer",
        "expires_in": 7200//过期时间（单位:秒）
    },
    "message": "登录成功"
}
```


> 抖音相关

**<span id='account_list'>2.账号列表</span>**

`url`：`{host}/api/open/douyin`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | page | 页码 | Y |  |

返回数据示例

```
{
    "code": 1,
    "data": {
        "data": [
            {
                "id": 14002,
                "uid": 56874100517,
                "account_id": "",
                "short_id": "7959561",
                "category_id": 5,
                "gender": 2,
                "nickname": "办公室小野",
                "avatar": "https://p9-dy.byteimg.com/aweme/100x100/fb2f00020a5cc52adb56.jpeg",
                "constellation": "5",
                "signature": "来围脖聊天吧：办公室小野 工作联系VX：k222k000。请说明公司/职位/项目",
                "verify_info": "",
                "city": "成都",
                "follows": 28,
                "fans": 2337.73,
                "douyin_fans_count": 15772778,
                "toutiao_fans_count": 5447332,
                "huoshan_fans_count": 2157153,
                "fans_val": 23377263,
                "digg": "9903.07",
                "digg_val": 99030693,
                "avg_digg": "458403.31",
                "comment": "1270248.00",
                "comment_val": "1270248.00",
                "avg_comment": 6383.16,
                "share": "1086736.00",
                "share_val": 1086736,
                "avg_share": 5461,
                "count": 199,
                "birthday": "1994-01-01",
                "like": 28,
                "with_douplus_entry": 0,
                "custom_verify": "",
                "music_count": 0,
                "with_fusion_shop_entry": 0,
                "status": 1,
                "updated_at": "2019-05-30 00:01:03",
                "created_at": "2018-10-31 19:34:43"
            },

            ...
        ],
        "has_more": true
    },
    "message": "成功"
}
```



**<span id='account_detail'>3.抖音账号详情</span>**

`url`：`{host}/api/open/douyin/detail`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | user_id | 排序 | N | 列表返回的uid |

```
{
    "code": 1,
    "data": {
        "user_id": "85089670734",
        "account_id": "GEMdzq",
        "short_id": "0",
        "nickname": "GEM鄧紫棋",
        "fans_count": 36604523,
        "digg_count": 232613353,
        "following_count": 0,
        "favoriting_count": 70,
        "count": 91,
        "gender": 1,
        "country": "Hong Kong",
        "province": "New Territories",
        "city": "Tsuen Wan",
        "location": "",
        "district": "",
        "signature": "歌手",
        "birthday": "1991-01-01",
        "constellation": 5,
        "avatar": "https://p3-dy.byteimg.com/aweme/720x720/bdcd000cfda1f334c442.jpeg",
        "home_link": "https://www.iesdouyin.com/share/user/85089670734",
        "custom_verify": "歌手、作词家、作曲家",
        "enterprise_verify_reason": "",
        "verification_type": 1,
        "is_gov_media_vip": false,
        "with_fusion_shop_entry": false,
        "is_star": true,
        "college_name": "",
        "music_used_count": 377800,
        "music_digg_count": 48703531,
        "music_count": 3
    },
    "message": "成功"
}

```


**<span id='video_list'>4.账号视频列表</span>**

`url`：`{host}/api/open/douyin/videos`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | user_id | 用户id | Y | 列表返回的uid |
| 2 | max_cursor | 排序 | N | 返回的max_cursor|

返回数据示例

```
{
    "code": 1,
    "data": {
        "videos": [
            {
                "aweme_id": "6794290129256107267",
                "duration": 6130,
                "is_top": 0,
                "create_time": 1581918951,
                "video_url": "https://www.iesdouyin.com/share/video/6794290129256107267/?region=CN&mid=6791292005559028487&u_code=0&titleType=title",
                "author_user_id": 85089670734,
                "title": "这么委婉地告诉我我丑😭😭😭 #侧颜",
                "group_id": "6794290129256107267",
                "preview_pic": "https://p3-dy.byteimg.com/img/tos-cn-p-0015/9c1cf1890c1849738614371980c105e4~c5_300x400.jpeg?from=2563711402_large",
                "width": 720,
                "height": 1280,
                "play_count": 0,
                "share_count": 8546,
                "digg_count": 2485945,
                "comment_count": 66674,
                "with_goods": 0,
                "author_nickname": "GEM鄧紫棋",
                "music_mid": 6791292005559028487,
                "music_name": "@菁菁是个小仙女创作的原声",
                "music_author_name": "菁菁是个小仙女",
                "music_author_id": "7176267155",
                "poi_id": "",
                "poi_name": "",
                "sticker_id": "",
                "sticker_name": ""
            },

            ...
      ],
        "has_more": 1,
        "max_cursor": 1580183576000
    },
    "message": "成功"
}
```


**<span id='video_detail'>5.视频详情</span>**

`url`：`{host}/api/open/douyin/video_detail`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | aweme_id | 视频id | Y | 视频列表返回的aweme_id |


返回参数示例

```
{
    "code": 1,
    "data": {
        "aweme_id": "6792195195359202574",
        "duration": 6250,
        "is_top": 0,
        "create_time": 1581431182,
        "video_url": "https://www.iesdouyin.com/share/video/6792195195359202574/?region=CN&mid=6787634339360328456&u_code=jfd9gf9h&titleType=title",
        "author_user_id": 62641621242,
        "title": "#重新认识一下，我姓黄，籍贯湖北武汉，身高169，体重98，外冷内热天蝎座，如果刷到我，你想对我说什么？",
        "group_id": "6792195195359202574",
        "preview_pic": "https://p3-dy.byteimg.com/img/tos-cn-p-0015/0eca17138f3c43c3af67229ac5cc9549~c5_300x400.jpeg?from=2563711402_large",
        "width": 720,
        "height": 1280,
        "play_count": 0,
        "share_count": 63,
        "digg_count": 10915,
        "comment_count": 8768,
        "with_goods": 0,
        "author_nickname": "曼妮",
        "music_mid": 6787634339360328456,
        "music_name": "用户创作的原声",
        "music_author_name": "久溺深海心会凉",
        "music_author_id": "105604326383",
        "poi_id": "",
        "poi_name": "",
        "sticker_id": "277931",
        "sticker_name": "烟雾"
    },
    "message": "成功"
}

```


**<span id='musics'>6.账号音乐列表</span>**

`url`：`{host}/api/open/douyin/musics`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | user_id | 用户id | Y | 列表返回的uid |
| 2 | cursor | 分页 | N |  |

返回参数示例

```
{
    "code": 1,
    "data": {
        "musics": [
            {
                "id": 6783131443376687117,
                "title": "无期",
                "duration": 117,
                "author": "光头华夏",
                "owner_id": "95741119273",
                "user_count": 161722,
                "avatar_thumb": "https://p3-dy.byteimg.com/aweme/100x100/2ec32000607f8f28a5bcd.jpeg",
                "cover_large": "https://p3-dy.byteimg.com/aweme/720x720/ies-music/storm_cover_66dd411902b789cdc02e7afe26e3bc74.jpeg",
                "play_url": "http://sf16-sg.muscdn.com/obj/tiktok-obj/1254ac4729e63c142b979f1d5e4d8319.mp3"
            },

            ...

        ],
        "has_more": 1,
        "cursor": 10
    },
    "message": "成功"
}
```


**<span id='music_videos'>7.音乐视频列表</span>**

`url`：`{host}/api/open/douyin/music_videos`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | music_id | 音乐id | Y | 列表返回的id |
| 2 | cursor | 分页 | N |  |

返回参数示例

```
{
    "code": 1,
    "data": {
        "videos": [
            {
                "aweme_id": "6787670385010806023",
                "duration": 33430,
                "is_top": 0,
                "create_time": 1580377677,
                "video_url": "https://www.iesdouyin.com/share/video/6787670385010806023/?region=CN&mid=6645303551079746318&u_code=kgkei6i7&titleType=title",
                "author_user_id": 84819817835,
                "title": "炖个汤喝喝😄😄",
                "group_id": "6787670385010806023",
                "preview_pic": "https://p1-dy.byteimg.com/img/tos-cn-p-0015/255ab9b4ba9a4013a7742fdd6cd74b21~c5_300x400.jpeg?from=2563711402_large",
                "width": 720,
                "height": 1280,
                "play_count": 0,
                "share_count": 0,
                "digg_count": 237,
                "comment_count": 47,
                "with_goods": 0,
                "author_nickname": "往事随风（靖江高尔夫瓷砖）",
                "music_mid": 6645303551079746318,
                "music_name": "过往云烟（副歌剪辑版）",
                "music_author_name": "光头华夏",
                "music_author_id": "95741119273",
                "poi_id": "6601124369315923976",
                "poi_name": "新营中学",
                "sticker_id": "",
                "sticker_name": ""
            },

            ...

          ],
        "has_more": 1,
        "cursor": 20
    },
    "message": "成功"
}
```


**<span id='hot_search'>8.抖音热搜榜</span>**

`url`：`{host}/api/open/douyin/hot_search`

请求参数：无

返回参数示例

```
{
    "code": 1,
    "data": [
        {
            "id": 1,
            "uri": "tos-cn-p-0015/6fee67bd66a5421896f3a75743fe7ed2",
            "word": "郑爽坦言暴瘦的原因",
            "hot_value": 10053933,
            "challenge_id": 0,
            "label": 0,
            "search_word": "",
            "created_at": "2020-02-19 14:00:02",
            "updated_at": "2020-02-19 14:00:02"
        },
        {
            "id": 2,
            "uri": "tos-cn-p-0015/6779d6919f2041aab1e7110e3708b464",
            "word": "去年底可能已有104名感染者",
            "hot_value": 6663605,
            "challenge_id": 0,
            "label": 0,
            "search_word": "",
            "created_at": "2020-02-19 14:00:02",
            "updated_at": "2020-02-19 14:00:02"
        },

        ...

      ],
    "message": "成功"
}
```


**<span id='hot_video'>9.今日最热视频</span>**

`url`：`{host}/api/open/douyin/hot_video`

请求参数：无

返回参数示例

```
{
    "code": 1,
    "data": [
        {
            "aweme_id": "6794806512574270733",
            "duration": 59050,
            "is_top": 0,
            "create_time": 1582039395,
            "video_url": "https://www.iesdouyin.com/share/video/6794806512574270733/?region=CN&mid=6794782167580904199&u_code=0&titleType=title",
            "author_user_id": 92837305962,
            "title": "法治社会，任何部门、任何人都不能因为戴着防控疫情的红袖标就可以任性妄为！",
            "group_id": "6794806512574270733",
            "preview_pic": "https://p9-dy.byteimg.com/img/tos-cn-p-0015/4f05c0ad11f04e14ba4ba168db7e4318~noop.jpeg?from=2563711402_large",
            "width": 720,
            "height": 1280,
            "play_count": 0,
            "share_count": 190996,
            "digg_count": 3606408,
            "comment_count": 112,
            "with_goods": 0,
            "author_nickname": "辽沈晚报",
            "music_mid": 6794782167580904199,
            "music_name": "@辽沈晚报创作的原声",
            "music_author_name": "辽沈晚报",
            "music_author_id": "92837305962",
            "poi_id": "",
            "poi_name": "",
            "sticker_id": "",
            "sticker_name": ""
        },

        ...

    ],
    "message": "成功"
}
```

**<span id='hot_music'>10.DOU听音乐榜</span>**

`url`：`{host}/api/open/douyin/hot_music`

请求参数：无

返回参数示例

```
{
    "code": 1,
    "data": [
        {
            "id": 6422856471440001793,
            "title": "舌尖上的中国",
            "duration": 48,
            "author": "阿鲲",
            "owner_id": "",
            "user_count": 4171091,
            "avatar_thumb": "",
            "cover_large": "https://p3-dy.byteimg.com/aweme/720x720/216a001ba103f68f6ffa.jpeg",
            "play_url": "http://p9-dy.byteimg.com/obj/29c8000023b5fb1c8b21"
        },

        ...

    ],
    "message": "成功"
}
```

**<span id='followings'>11.关注列表</span>**

`url`：`{host}/api/open/douyin/followings`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | user_id | 用户id | Y | 列表返回的uid |
| 2 | max_time | 分页 | N |  |

返回参数示例

```
{
    "code": 1,
    "data": {
        "followings": [
            {
                "user_id": "68310389333",
                "account_id": "",
                "short_id": "71158770",
                "nickname": "李子柒",
                "fans_count": 0,
                "digg_count": 0,
                "following_count": 0,
                "favoriting_count": 0,
                "count": 0,
                "gender": 2,
                "country": "",
                "province": "",
                "city": "",
                "location": "",
                "district": "",
                "signature": "李家有女，人称子柒",
                "birthday": "",
                "constellation": 0,
                "avatar": "https://p3-dy.byteimg.com/aweme/720x720/330b002fd56a93e8b6f1.heic",
                "home_link": "https://www.iesdouyin.com/share/user/68310389333",
                "custom_verify": "美食自媒体",
                "enterprise_verify_reason": "",
                "verification_type": 1,
                "is_gov_media_vip": false,
                "with_fusion_shop_entry": true,
                "is_star": "",
                "college_name": "",
                "music_used_count": 0,
                "music_digg_count": 0,
                "music_count": 0
            },
            ...
        ],
        "has_more": true,
        "max_time": 1566779587
    },
    "message": "成功"
}
```

**<span id='followers'>12.粉丝列表</span>**

`url`：`{host}/api/open/douyin/followings`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | user_id | 用户id | Y | 列表返回的uid |
| 2 | min_time | 分页 | N |  |

返回参数示例

```
{
    "code":1,
    "data":{
        "followings":[
            {
                "user_id":"92658052801",
                "account_id":"",
                "short_id":"342164711",
                "nickname":"94的老年人",
                "fans_count":0,
                "digg_count":0,
                "following_count":0,
                "favoriting_count":0,
                "count":0,
                "gender":0,
                "country":"",
                "province":"",
                "city":"",
                "location":"",
                "district":"",
                "signature":"",
                "birthday":"",
                "constellation":0,
                "avatar":"https://p3.pstatp.com/thumb/5d500024f23306bab684",
                "home_link":"https://www.iesdouyin.com/share/user/92658052801",
                "custom_verify":"",
                "enterprise_verify_reason":"",
                "verification_type":1,
                "is_gov_media_vip":false,
                "with_fusion_shop_entry":false,
                "is_star":"",
                "college_name":"",
                "music_used_count":0,
                "music_digg_count":0,
                "music_count":0
            },
            ...
        ],
        "has_more":true,
        "min_time":1566613803
    },
    "message":"成功"
}
```

**<span id='comments'>13.评论列表</span>**

`url`：`{host}/api/open/douyin/comments`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | aweme_id | 视频id | Y | 列表返回的aweme_id |
| 2 | cursor | 分页 | N |  |

返回参数示例

```
{
    "code":1,
    "data":{
        "comments":[
            {
                "aweme_id":"6617375060703317255",
                "text":"这姿势真的不行",
                "create_time":"2020-02-04 05:26:21",
                "digg_count":5,
                "uid":"2273442056379428",
                "nickname":"小民"
            },
            ...
        ],
        "has_more":1,
        "cursor":21
    },
    "message":"成功"
}
```

**<span id='feeds'>14.feeds</span>**

`url`：`{host}/api/open/douyin/feeds`

请求参数:无

返回参数示例

```
{
    "code":1,
    "data":[
        {
            "aweme_id":"6794763458891091207",
            "duration":35430,
            "is_top":0,
            "create_time":1582029151,
            "video_url":"https://www.iesdouyin.com/share/video/6794763458891091207/?region=CN&mid=6794745906479729421&u_code=0&titleType=title",
            "author_user_id":75947711733,
            "title":"痛经必练瑜伽，比红糖水管用！#痛经 #居家健身抖出花样",
            "group_id":"6794763458891091207",
            "preview_pic":"http://p9-dy.byteimg.com/large/tos-cn-p-0015/e4e2b82d4b0f442399ffe107d2e9e5f0.jpeg?from=2563711402_large",
            "width":720,
            "height":1280,
            "play_count":0,
            "share_count":2930,
            "digg_count":19352,
            "comment_count":739,
            "with_goods":0,
            "author_nickname":"JJYOGA瑜伽",
            "music_mid":6794745906479729421,
            "music_name":"@JJYOGA瑜伽创作的原声",
            "music_author_name":"JJYOGA瑜伽",
            "music_author_id":"75947711733",
            "poi_id":"",
            "poi_name":"",
            "sticker_id":"",
            "sticker_name":""
        },
    ...
    ],
    "message":"成功"
}
```

**<span id='challengets'>15.挑战列表</span>**

`url`：`{host}/api/open/douyin/challengets`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | cursor | 分页 | N |  |

返回参数示例

```
{
    "code":1,
    "data":{
        "challengets":[
            {
                "cha_name":"对嘴型",
                "desc":"选一首歌来对嘴型，看谁对的最像",
                "cid":"1550886680026114"
            },
            {
                "cha_name":"我也有属于自己的片尾了",
                "desc":"",
                "cid":"1658849233565709"
            },

            ...

          ],
        "has_more":1,
        "cursor":12
    },
    "message":"成功"
}
```

**<span id='challenget_detail'>16.挑战详情</span>**

`url`：`{host}/api/open/douyin/challenget_detail`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | keyword | 挑战名称| Y | 列表里cha_name字段 |

返回参数示例

```
{
    "code": 1,
    "data": {
        "cha_name": "线上不打烊",
        "desc": "",
        "cid": "1657316898838540",
        "cover": "https://p9-dy.byteimg.com/obj/2f7ab0001cd59da2ca862?from=568394430",
        "user_count": 214,
        "view_count": 4797395,
        "author_uid": "75516232460",
        "author_nickname": "Vicky"
    },
    "message": "成功"
}
```


**<span id='challenget_videos'>17.挑战视频列表</span>**

`url`：`{host}/api/open/douyin/challenget_videos`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | keyword | 挑战名| Y | 列表里cha_name字段 |
| 2 | cursor | 分页 | N |  |

返回参数示例

```
{
    "code":1,
    "data":{
        "videos":[
            {
                "aweme_id":"6794346251325410560",
                "duration":20300,
                "is_top":0,
                "create_time":1581932013,
                "video_url":"https://www.iesdouyin.com/share/video/6794346251325410560/?region=CN&mid=6793857987070642957&u_code=0&titleType=title",
                "author_user_id":66001253867,
                "title":"#宅家遛娃趣味大pk",
                "group_id":"6794346251325410560",
                "preview_pic":"https://p9-dy.byteimg.com/img/tos-cn-p-0015/3596ed77c1d7438fa7f8fb2e5d513d25~noop.jpeg?from=2563711402_large",
                "width":720,
                "height":1280,
                "play_count":0,
                "share_count":1,
                "digg_count":22,
                "comment_count":2,
                "with_goods":0,
                "author_nickname":"黑白灰",
                "music_mid":6793857987070642957,
                "music_name":"@一只肉橙创作的原声",
                "music_author_name":"一只肉橙",
                "music_author_id":"1200301315462088",
                "poi_id":"",
                "poi_name":"",
                "sticker_id":"",
                "sticker_name":""
            },
            ...
        ],
        "has_more":1,
        "cursor":54
    },
    "message":"成功"
}
```

**<span id='sticker_info'>18.贴纸详情</span>**

`url`：`{host}/api/open/douyin/sticker_info`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | sticker_ids | 贴纸id| Y | 视频列表里sticker_id字段(多个id用逗号（,）链接 例: 522844,277931) |

返回参数示例

```
{
    "code": 1,
    "data": [
        {
            "id": "522844",
            "name": "结婚男女",
            "owner_id": "96972139640",
            "owner_nickname": "抖音魔法道具",
            "owner_avatar": "https://p3-dy.byteimg.com/aweme/1080x1080/a65000190294042ddf7c.jpeg",
            "view_count": 1892883193,
            "user_count": 5068938,
            "icon_url": "https://lf3-effectcdn-tos.pstatp.com/obj/ies.fe.effect/6d689ccc803b0c057132f586e7ad26e4"
        },
        {
            "id": "277931",
            "name": "烟雾",
            "owner_id": "96972139640",
            "owner_nickname": "抖音魔法道具",
            "owner_avatar": "https://p3-dy.byteimg.com/aweme/1080x1080/a65000190294042ddf7c.jpeg",
            "view_count": 98676564171,
            "user_count": 34396531,
            "icon_url": "https://lf3-effectcdn-tos.pstatp.com/obj/ies.fe.effect/1e0ebfb003623f7ecc2bc06208909233"
        }
    ],
    "message": "成功"
}
```

**<span id='sticker_videos'>19.贴纸视频列表</span>**

`url`：`{host}/api/open/douyin/sticker_videos`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | sticker_id | 贴纸id| Y | 视频列表里sticker_id字段|
| 2 | cursor | 分页| N | |

返回参数示例

```
{
    "code":1,
    "data":{
        "videos":[
            {
                "aweme_id":"6793843155847351559",
                "duration":10170,
                "is_top":0,
                "create_time":1581814880,
                "video_url":"https://www.iesdouyin.com/share/video/6793843155847351559/?region=CN&mid=6791814288848816904&u_code=0&titleType=title",
                "author_user_id":61907723177,
                "title":"24岁结婚，25岁生了双胞胎，老公挣钱不多但是顾家，公婆明事理，儿子懂事，农村有楼，城里有房，这是幸福吗#热门",
                "group_id":"6793843155847351559",
                "preview_pic":"https://p3-dy.byteimg.com/img/tos-cn-p-0015/06f4d4fe7a104811b1ef4998567893de~c5_300x400.jpeg?from=2563711402_large",
                "width":720,
                "height":1280,
                "play_count":0,
                "share_count":182,
                "digg_count":72678,
                "comment_count":4125,
                "with_goods":0,
                "author_nickname":"双胞胎辰溪妈妈",
                "music_mid":6791814288848816904,
                "music_name":"星月神话",
                "music_author_name":"懒惰猫",
                "music_author_id":"94932532349",
                "poi_id":"",
                "poi_name":"",
                "sticker_id":"522844",
                "sticker_name":"结婚男女"
            },
            ...
        ],
        "has_more":1,
        "cursor":18
    },
    "message":"成功"
}
```

**<span id='favorite'>20.收藏列表</span>**

`url`：`{host}/api/open/douyin/favorite`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | user_id | 贴纸id| Y | 账号列表里uid字段|
| 2 | max_cursor | 分页| N | |

返回参数示例

```
{
    "code":1,
    "data":{
        "videos":[
            {
                "aweme_id":"6789098122401303808",
                "duration":12100,
                "is_top":0,
                "create_time":1580710087,
                "video_url":"https://www.iesdouyin.com/share/video/6789098122401303808/?region=CN&mid=6786061090611530499&u_code=i082b75d&titleType=title",
                "author_user_id":58555378449,
                "title":"仙境大概就是这样了吧",
                "group_id":"6789098122401303808",
                "preview_pic":"https://p3-dy.byteimg.com/img/tos-cn-p-0015/fdab7e7abe5649fd882cf1ad4208367f~c5_300x400.jpeg?from=2563711402_large",
                "width":640,
                "height":800,
                "play_count":0,
                "share_count":10707,
                "digg_count":310781,
                "comment_count":19646,
                "with_goods":0,
                "author_nickname":"Lucifer",
                "music_mid":6786061090611530499,
                "music_name":"@Lucifer创作的原声",
                "music_author_name":"Lucifer",
                "music_author_id":"58555378449",
                "poi_id":"",
                "poi_name":"",
                "sticker_id":"",
                "sticker_name":""
            },

            ...
        ],
        "has_more":1,
        "max_cursor":1579360370000
    },
    "message":"成功"
}
```

**<span id='nearby'>21.附近人</span>**

`url`：`{host}/api/open/douyin/nearby`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | city | 城市code| Y | 北京:110000|
| 2 | longitude |经度| N | |
| 3 | latitude | 纬度| N | |

返回参数示例

```
{
    "code":1,
    "data":{
        "videos":[
            {
                "aweme_id":"6794354574170950920",
                "duration":71490,
                "is_top":0,
                "create_time":1581933995,
                "video_url":"https://www.iesdouyin.com/share/video/6794354574170950920/?region=CN&mid=6794340656124054286&u_code=0&titleType=title",
                "author_user_id":65590091849389,
                "title":"遇见这样的事儿，你心动吗？#剧情 #防骗 #战胜疫情dou行动",
                "group_id":"6794354574170950920",
                "preview_pic":"https://p3-dy.byteimg.com/img/tos-cn-p-0015/0936ccd720f943808aaa59e95445f299_1581934024~noop.jpeg?from=2563711402_large",
                "width":1080,
                "height":1920,
                "play_count":0,
                "share_count":143,
                "digg_count":12464,
                "comment_count":142,
                "with_goods":0,
                "author_nickname":"神探大妈",
                "music_mid":6794340656124054286,
                "music_name":"@神探大妈创作的原声",
                "music_author_name":"神探大妈",
                "music_author_id":"65590091849389",
                "poi_id":"",
                "poi_name":"",
                "sticker_id":"",
                "sticker_name":""
            },
            ...
       ],
        "has_more":1
    },
    "message":"成功"
}
```

**<span id='poi_detail'>22.定位信息</span>**

`url`：`{host}/api/open/douyin/poi_detail`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | poi_id | 定位id| Y | 视频列表里poi_id字段|
| 2 | longitude |经度| N | |
| 3 | latitude | 纬度| N | |

返回参数示例

```
{
    "code": 1,
    "data": {
        "corver": "https://p3-dy.byteimg.com/img/f6f80008c5d072008164~q40.jpeg?from=1551292344",
        "user_count": 201631545,
        "view_count": "108923369400",
        "item_count": 10357210,
        "poi_name": "北京市",
        "province": "北京市",
        "city": "北京市",
        "district": "",
        "address": "",
        "city_code": "110000"
    },
    "message": "成功"
}
```

**<span id='poi_videos'>23.定位信息视频列表</span>**

`url`：`{host}/api/open/douyin/poi_videos`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | poi_id | 定位id| Y | 视频列表里poi_id字段|
| 2 | longitude |经度| N | |
| 3 | latitude | 纬度| N | |
| 4 | cursor | 分页| N | |

返回参数示例

```
{
    "code":1,
    "data":{
        "videos":[
            {
                "aweme_id":"6738324786830675204",
                "duration":44980,
                "is_top":0,
                "create_time":1568888501,
                "video_url":"https://www.iesdouyin.com/share/video/6738324786830675204/?region=CN&mid=6738295205063035656&u_code=kgkdk379&titleType=title",
                "author_user_id":77086118738,
                "title":"北京远比你想的好玩的多，这些地方你知道吗？#我的家乡真you味 #welcometo",
                "group_id":"6738324786830675204",
                "preview_pic":"https://p9-dy.byteimg.com/img/tos-cn-p-0015/4e5aad9b63674a02af7c9cf8ccf3d1aa~c5_300x400.jpeg?from=2563711402_large",
                "width":720,
                "height":1280,
                "play_count":0,
                "share_count":6930,
                "digg_count":63928,
                "comment_count":2852,
                "with_goods":0,
                "author_nickname":"二娃千里看世界",
                "music_mid":6738295205063035656,
                "music_name":"@二娃千里看世界创作的原声",
                "music_author_name":"二娃千里看世界",
                "music_author_id":"77086118738",
                "poi_id":"6601142635132356621",
                "poi_name":"郎园Park",
                "sticker_id":"",
                "sticker_name":""
            },
            ...
        ],
        "has_more":1,
        "cursor":10
    },
    "message":"成功"
}
```

**<span id='live_list'>24.直播列表</span>**

`url`：`{host}/api/open/douyin/live_list`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | max_time | 分页| Y | |

返回参数示例

```
{
    "code":1,
    "data":{
        "lives":[
            {
                "cover":"http://p6-webcast-dycdn.byteimg.com/img/webcast/6756132007736134403~tplv-resize:400:400.jpeg",
                "create_time":1582099272,
                "finish_time": 1582099886,
                "id":6795064632265411343,
                "owner_user_id":70746034234,
                "share_url":"https://www.iesdouyin.com/share/live/6795064632265411343",
                "stream_id":6795060538247367439,
                "title":"唱歌给你听",
                "rid":"20200219160737010129020212290A3475",
                "user_count":567
            },
            ...
        ],
        "max_time":1582099658079
    },
    "message":"成功"
}
```

**<span id='live_rank'>25.直播礼物榜</span>**

`url`：`{host}/api/open/douyin/live_rank`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | room | 分页| Y |直播列表返回的 id 字段|
| 2 | user_id | 分页| Y |直播列表返回的owner_user_id字段 |

返回参数示例

```
{
    "code":1,
    "data":{
        "ranks":[
            {
                "gap_description":"1041",
                "rank":1,
                "score":1041,
                "uid":698887620532035,
                "account_id":"hebe33003",
                "nickname":"赚钱养一一",
                "short_id":2342049472,
                "gender":0,
                "avatar":"https://p9-dy.byteimg.com/aweme/100x100/2f54c00037598d0fd689a.jpeg",
                "level":39,
                "total_score":732711
            },
            ...
        ],
        "total":1047
    },
    "message":"成功"
}

```

**<span id='live_promotions'>26.直播购物车</span>**

`url`：`{host}/api/open/douyin/live_promotions`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | room | 分页| Y |直播列表返回的 id 字段|
| 2 | user_id | 分页| Y |直播列表返回的owner_user_id字段 |

返回参数示例

```
{
    "code": 1,
    "data": {
        "promotions": [
            {
                "promotion_id": "3381948298066831740",
                "product_id": "3381947396173997771",
                "shop_id": 290614,
                "promotion_source": 4,
                "title": "雷霸简易快接水龙头外加喷头套装卫生间手持洗头神器水嘴接头2.2",
                "cos_fee": 812,
                "cos_ratio": 28,
                "price": 2900,
                "cover": "https://sf6-ttcdn-tos.pstatp.com/img/temai/FtwKD0Ss_x4lQR0TmIxhzsJs-w-bwww1080-1080~tplv-resize:200:0.webp"
            },
            {
                "promotion_id": "3380607286920755549",
                "product_id": "3380605405725068996",
                "shop_id": 322596,
                "promotion_source": 4,
                "title": " 【每日好货】GF·谷猫GUCAT 厨房垃圾桶家用橱柜门折叠悬可挂式",
                "cos_fee": 1346,
                "cos_ratio": 45,
                "price": 2990,
                "cover": "https://sf6-ttcdn-tos.pstatp.com/img/temai/FgFgKMUfm-Sqe60jJssPqtdNYiquwww750-1000~tplv-resize:200:0.webp"
            },
            ...
        ],
        "has_more": false
    },
    "message": "成功"
}
```



**<span id='promotions'>27.橱窗商品列表</span>**

`url`：`{host}/api/open/douyin/promotions`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | user_id | 用户id | Y |账号列表返回的 uid 字段|
| 2 | cursor | 分页| N | |

返回参数示例

```
{
    "code":1,
    "data":{
        "promotion":{
            "0":{
                "promotion_id":"3326121677683871125",
                "product_id":"586413328330",
                "shop_id":"",
                "sales":1205,
                "promotion_source":7,
                "clicks":0,
                "elastic_type":3,
                "title":"JG军哥太极八卦球黑白室内室外真皮手感比赛训练标准七号个性篮球",
                "last_aweme_id":"6784246701273271560",
                "cos_fee":1662,
                "favorited":true,
                "elastic_title":"JG太极八卦篮球球",
                "rank":0,
                "cos_radio":0,
                "market_price":11875,
                "url":"",
                "views":0,
                "elastic_introduction":"",
                "price":11875,
                "h5_url":"",
                "rank_url":"",
                "label":true,
                "count":0,
                "imgs":"",
                "cover":""
            },
            ...
        },
        "has_more":true,
        "count":40
    },
    "message":"成功"
}
```

**<span id='product'>28.商品详情</span>**

`url`：`{host}/api/open/douyin/product`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | user_id | 用户id | Y |账号列表返回的 uid 字段|
| 2 | product_id | 商品id| Y |橱窗列表返回的 product_id 字段 |
| 3 | promotion_id | promotion_id| Y |橱窗列表返回的 promotion_id 字段 |

返回参数示例

```
{
    "code": 1,
    "data": {
        "promotion_id": "3381948298066831740",
        "product_id": "3381947396173997771",
        "shop_id": "",
        "sales": 17278,
        "promotion_source": 4,
        "clicks": 0,
        "elastic_type": 0,
        "title": "雷霸简易快接水龙头外加喷头套装卫生间手持洗头神器水嘴接头2.2",
        "last_aweme_id": "",
        "cos_fee": 812,
        "favorited": false,
        "elastic_title": "",
        "rank": 0,
        "cos_radio": 0,
        "market_price": 2900,
        "url": "",
        "views": 0,
        "elastic_introduction": "",
        "price": 2900,
        "h5_url": "",
        "rank_url": "",
        "label": "",
        "count": 0,
        "imgs": "",
        "cover": ""
    },
    "message": "成功"
}
```

**<span id='order_share'>29.商品晒单列表</span>**

`url`：`{host}/api/open/douyin/order_share`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | promotion_id | promotion_id| Y |橱窗列表返回的 promotion_id 字段 |
| 2 | page | 分页| N |从0开始 |

返回参数示例

```
{
    "code": 1,
    "data": {
        "videos": [
            {
                "aweme_id": "6787286815524113676",
                "duration": 12450,
                "is_top": 0,
                "create_time": 1580288371,
                "video_url": "https://www.iesdouyin.com/share/video/6787286815524113676/?region=CN&mid=6787278642352884483&u_code=0&titleType=title",
                "author_user_id": 3460890833458020,
                "title": "军哥我这是真球吗",
                "group_id": "6787286815524113676",
                "preview_pic": "https://p3-dy.byteimg.com/img/tos-cn-p-0015/5c6463512e2f46c6acdf1908c35b5a17~c5_300x400.jpeg?from=2563711402_large",
                "width": 576,
                "height": 1024,
                "play_count": 0,
                "share_count": 0,
                "digg_count": 1,
                "comment_count": 1,
                "with_goods": 1,
                "author_nickname": "用户268438969",
                "music_mid": 6787278642352884483,
                "music_name": "@用户268438969创作的原声",
                "music_author_name": "用户268438969",
                "music_author_id": "3460890833458020",
                "poi_id": "",
                "poi_name": "",
                "sticker_id": "",
                "sticker_name": ""
            },
            ...
        ],
        "$total": 5
    },
    "message": "成功"
}
```


**<span id='product_comments'>30.商品评价列表</span>**

`url`：`{host}/api/open/douyin/product_comments`

请求参数

| 编号 | 字段 | 名称 | 是否必须 | 备注 |
| --- | --- | --- | --- |--- |
| 1 | promotion_id | promotion_id| Y |橱窗列表返回的 promotion_id 字段 |
| 2 | product_id | 商品id| Y |橱窗列表返回的 product_id 字段 |
| 3 | page | 分页| N |从0开始 |

返回参数示例

```
{
    "code":1,
    "data":{
        "videos":[
            {
                "user_name":"关**奇",
                "user_avatar":"http://p0.pstatp.com/origin/3795/3047680722",
                "content":"看住不赖！穿上包裹和缓震都不错！军哥还送了一双袜子！",
                "comment_time":"2019-12-19 11:53:04",
                "sku":"黑/绯红/荧光魅力紫/45",
                "rank_product":"4",
                "rank":12,
                "likes":2,
                "photos":[
                    "https://sf3-ttcdn-tos.pstatp.com/img/2e7b00006e8d64e8999d9~960x0.image",
                    "https://sf3-ttcdn-tos.pstatp.com/img/2e7d300033f7a8da6f85e~960x0.image",
                    "https://sf1-ttcdn-tos.pstatp.com/img/2e7230005b2e282b1923e~960x0.image",
                    "https://sf1-ttcdn-tos.pstatp.com/img/2e7b70005420f700e5624~960x0.image"
                ]
            },
        ...
        ],
        "total":8
    },
    "message":"成功"
}
```

