# 树洞有声

## 实体类设计

```java
public class Blog {

    private Integer id;

    private Integer userId;

    private String title;

    private String content;

    //拥抱/点赞
    private Integer hug;

    //发布时间
    private Date releaseTime;

    //是否可评论，默认可评论
    private Boolean evaluable;

    //是否公开，默认公开
    private Boolean state;

    private Boolean valid;
}
```
```java
public class Comment {
    private Integer id;

    private Integer userId;

    private Integer blogId;

    private String content;

    private Integer thank;

    //是否为私信，默认false
    private Boolean state;

    //是否被举报
    private Boolean tipOff;

    private Boolean valid;
}
```
```java
public class User {

    private Integer id;

    //微信小程序唯一id
    private String openId;

    private Integer address;

    private String nickName;

    private Boolean valid;
}
```
## 统一响应格式

```java
public class HoleResult {

    private int code;

    private String message;

    private Object data;
}
```