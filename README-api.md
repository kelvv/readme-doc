# Brief

### headers:

|        **name**         |       **value**       |
| :-----------------      | :-------------------: |
|  x-authorization-token  |          token        |
|  x-app-platform         |     web , web-admin   |
|  x-app-error            |     true , false      |

### querys:

|        **name**         |       **detail**       |
| :-----------------      | :-------------------: |
|        sort             |          排序           |
|        limit            |       限制返回数量（分页） |
|        skip             |       跳过返回数量（分页） |


#### error code table:

| **code** | **detial** | 
|:---|:---:|
| 403 | Access denied |
| 404 | Not Found |
| 422 | Invalid data |
| 429 | 请勿在短时间内多次尝试 |
| 430 | 短信服务出现故障，正在进行修复 |
| 501 | 暂时不可用 |
| 1001 | Illegal token |



# Models


## 1.1  Banner  
##### Structure: 
```


Banner = {
    link: String,
    title: String,
    isValid: {
        type: Boolean,
        default: true
    }
}
 
```


## 1.2  User  
##### Structure: 
```


User = {
    openId: String,
    nickname: String,
    isValid: {
        type: Boolean,
        default: true
    }
}
 
```




# ***** ACCOUNT *****

#### POST  /account/signin/wechat  
``` 
 /*
    body : {
        openId   : string,
        regionId : objectId,
    }
*/

```
#### GET  /region/:_regionId/login/historys  
``` 
 /*
    params : {
        _regionId    : objectId
    }
*/

```

# ***** REGION *****

#### PUT  /region/:_id  
``` 
 /*
    params : {
        _id   : objectId
    }

    body : {
        name   : string,
        state  : string   //'1','2'
    }
*/

```