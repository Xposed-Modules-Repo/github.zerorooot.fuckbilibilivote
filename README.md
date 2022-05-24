# FuckBilibiliVote
移除哔哩哔哩app中的vote(投票) 、attention(一键三连)和link(预告)

[![Total Stars](https://img.shields.io/github/stars/zerorooot/FuckBilibiliVote?style=social)](https://github.com/zerorooot/FuckBilibiliVote/) [![Latest Release](https://img.shields.io/github/v/release/zerorooot/FuckBilibiliVote?label=Latest%20Release)](https://github.com/zerorooot/FuckBilibiliVote/releases)

勾选后查看lsp日志，输出以下内容即为hook成功

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
