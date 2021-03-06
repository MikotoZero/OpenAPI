# `message` 事件

## 被动接收

```
{
  "created_ts": 1487570962851,
  "image": "",
  "key": "1487570962851.0148",
  "refer_key": null,
  "subtype": "normal",
  "text": "test",
  "to_uid": "=bwCkD",
  "ts": 1487570962851,
  "type": "message",
  "uid": "=bwFrB",
  "vchannel_id": "=515SFkkX"
}
```

message 事件在 P2P 会话中收到新消息的时候触发。其中 `uid` 为消息发送者 id,
`to_uid` 为消息接收者 id, `vchannel_id` 为对应会话 id, `key` 为消息 key.


## 主动发送

```
{
  "vchannel_id": "=515SFkkX",
  "text": "test",
  "type": "message",
  "to_uid": "=bwCkD",
  "refer_key": null,
  "call_id": 1
}
```

### 字段说明

| 字段 | 类型 | 说明 |
|:----:|:----:|------|
| `vchannel_id` | `string` | P2P 会话 id，**必填** |
| `text` | `string` | 消息内容，**必填** |
| `type` | `MessageType` | 消息类型，P2P 消息值为 `message`， **必填** |
| `to_uid` | `string` | 接收用户 id, **必填** |
| `refer_key` | `Optional<string>` | 引用消息 id, 没有引用消息时值为 `null`,  **必填** |
| `call_id` | `int` | 事件序列 id **必填** |
