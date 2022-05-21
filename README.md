# FuckBilibiliVote
移除哔哩哔哩app中的vote(投票) 、attention(一键三连)和link(预告)

[![Total Stars](https://img.shields.io/github/stars/zerorooot/FuckBilibiliVote?style=social)](https://github.com/zerorooot/FuckBilibiliVote/) [![Latest Release](https://img.shields.io/github/v/release/zerorooot/FuckBilibiliVote?label=Latest%20Release)](https://github.com/zerorooot/FuckBilibiliVote/releases)

<img src="https://raw.githubusercontent.com/zerorooot/FuckBilibiliVote/main/Screenshot/demo.jpg" width="50%">

# 下载
https://github.com/zerorooot/FuckBilibiliVote/releases

# 如何自定义

## 找到相关类和方法

反编译app，搜索

```
import com.bapis.bilibili.app.view.v1.CommandDm;
```

或者

```
com/bapis/bilibili/app/view/v1/CommandDm
```

找有类似下面这段代码的方法

```java
viewProgressChange$CommandDM.setId(String.valueOf(commandDm.getId()));
viewProgressChange$CommandDM.setOid(Long.valueOf(commandDm.getOid()));
viewProgressChange$CommandDM.setMid(Long.valueOf(commandDm.getMid()));
viewProgressChange$CommandDM.setCommand(commandDm.getCommand());
viewProgressChange$CommandDM.setContent(commandDm.getContent());
viewProgressChange$CommandDM.setProgress(Integer.valueOf(commandDm.getProgress()));
viewProgressChange$CommandDM.setCtime(commandDm.getCtime());
viewProgressChange$CommandDM.setMtime(commandDm.getMtime());
viewProgressChange$CommandDM.setExtra(commandDm.getExtra());
arrayList2.add(viewProgressChange$CommandDM);
```

比如在6.73.1，方法的名字是`m0`

```java
private final void m0(ViewProgressReply viewProgressReply, long j2, long j3) {}
```

![guide](https://raw.githubusercontent.com/zerorooot/FuckBilibiliVote/main/Screenshot/guide.png)

记下当前的类名和方法

类名  :`tv.danmaku.chronos.wrapper.chronosrpc.remote.RemoteServiceHandler`

方法 : `m0`

## 在app里设置类名和方法

把刚才得到的类名和方法填入biliClassName和biliClassMethod中，保存

<img src="https://raw.githubusercontent.com/zerorooot/FuckBilibiliVote/main/Screenshot/demo.jpg" width="50%">

重启哔哩哔哩

打开相关视频

查看lsp日志，输出以下内容即为hook成功

```
arc_shot {
  image: "x"
  img_x_len: 10
  img_x_size: 160
  img_y_len: 10
  img_y_size: 90
  pv_data: "x"
}
chronos {
  file: "x"
  md5: "x"
  sign: "x"
}
video_guide {
  attention {
    end_time: 52
    pos_x: 499.39030955585457
    pos_y: 292.0188425302826
    start_time: 47
  }
  command_dms {
    command: "#VOTE#"
    content: "x"
    ctime: "2022-04-29 18:04:00"
    extra: "{x}"
    id: 1041323547978519296
    id_str: "1041323547978519296"
    mid: 52933528
    mtime: "2022-05-13 19:17:50"
    oid: 587789591
    progress: 18300
  }
  command_dms {
    command: "#ATTENTION#"
    content: "x"
    ctime: "2022-04-29 18:04:37"
    extra: "{x}"
    id: 1041323858281438208
    id_str: "1041323858281438208"
    mid: 52933528
    mtime: "2022-04-29 18:04:37"
    oid: 587789591
    progress: 47500
  }
  command_dms {
    command: "#LINK#"
    content: "x"
    ctime: "2022-05-05 18:58:04"
    extra: "{xxx}"
    id: 1045699414951301120
    id_str: "1045699414951301120"
    mid: 52933528
    mtime: "2022-05-05 18:58:15"
    oid: 587789591
    progress: 59000
  }
}
```

