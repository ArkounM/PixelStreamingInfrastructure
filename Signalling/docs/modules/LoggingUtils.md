[@epicgames-ps/lib-pixelstreamingsignalling-ue5.5](../README.md) / LoggingUtils

# Module: LoggingUtils

## Table of contents

### Interfaces

- [IMessageLogger](../interfaces/LoggingUtils.IMessageLogger.md)
- [IProtoLogObj](../interfaces/LoggingUtils.IProtoLogObj.md)

### Functions

- [createHandlerListener](LoggingUtils.md#createhandlerlistener)
- [logForward](LoggingUtils.md#logforward)
- [logIncoming](LoggingUtils.md#logincoming)
- [logOutgoing](LoggingUtils.md#logoutgoing)

## Functions

### createHandlerListener

▸ **createHandlerListener**(`obj`, `handler`): (`message`: `BaseMessage`) => `void`

We don't want to log every incoming and outgoing messages. This is because some messages are simply
forwarded to other connections. This results in duplicated spam. So we only want to log incoming
messages that we handle internally, and any messages that we forward we only log once for the recv
and send events.
This creation method allows a simple way to enforce this. Any events we handle directly will
be preceded by the logging call.

#### Parameters

| Name | Type |
| :------ | :------ |
| `obj` | [`IMessageLogger`](../interfaces/LoggingUtils.IMessageLogger.md) |
| `handler` | (`message`: `any`) => `void` |

#### Returns

`fn`

▸ (`message`): `void`

##### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `BaseMessage` |

##### Returns

`void`

#### Defined in

[Signalling/src/LoggingUtils.ts:74](https://github.com/mcottontensor/PixelStreamingInfrastructure/blob/709d6fe/Signalling/src/LoggingUtils.ts#L74)

___

### logForward

▸ **logForward**(`recvr`, `target`, `message`): `void`

Call this for messages being forwarded to this connection. That is messages received on
one connection and being sent to another with only minor changes being made.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `recvr` | [`IMessageLogger`](../interfaces/LoggingUtils.IMessageLogger.md) | The connection the message was received on. |
| `target` | [`IMessageLogger`](../interfaces/LoggingUtils.IMessageLogger.md) | The connection the message is being sent to. |
| `message` | `BaseMessage` | - |

#### Returns

`void`

#### Defined in

[Signalling/src/LoggingUtils.ts:56](https://github.com/mcottontensor/PixelStreamingInfrastructure/blob/709d6fe/Signalling/src/LoggingUtils.ts#L56)

___

### logIncoming

▸ **logIncoming**(`recvr`, `message`): `void`

Call to log messages received on a connection that we will handle here at the server.
Do not call this for messages being forwarded to another connection.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `recvr` | [`IMessageLogger`](../interfaces/LoggingUtils.IMessageLogger.md) | IMessageLogger The connection the message was received on. |
| `message` | `BaseMessage` | - |

#### Returns

`void`

#### Defined in

[Signalling/src/LoggingUtils.ts:26](https://github.com/mcottontensor/PixelStreamingInfrastructure/blob/709d6fe/Signalling/src/LoggingUtils.ts#L26)

___

### logOutgoing

▸ **logOutgoing**(`sender`, `message`): `void`

Call to log messages created here at the server and being sent to the connection.
Do not call this for messages being forwarded to this connection.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `sender` | [`IMessageLogger`](../interfaces/LoggingUtils.IMessageLogger.md) | IMessageLogger The connection the message is being sent to. |
| `message` | `BaseMessage` | - |

#### Returns

`void`

#### Defined in

[Signalling/src/LoggingUtils.ts:41](https://github.com/mcottontensor/PixelStreamingInfrastructure/blob/709d6fe/Signalling/src/LoggingUtils.ts#L41)
