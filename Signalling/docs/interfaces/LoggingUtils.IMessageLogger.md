[@epicgames-ps/lib-pixelstreamingsignalling-ue5.5](../README.md) / [LoggingUtils](../modules/LoggingUtils.md) / IMessageLogger

# Interface: IMessageLogger

[LoggingUtils](../modules/LoggingUtils.md).IMessageLogger

Most methods in here rely on connections implementing this interface so we can identify
who is sending or receiving etc.

## Hierarchy

- **`IMessageLogger`**

  ↳ [`IPlayer`](PlayerRegistry.IPlayer.md)

  ↳ [`IStreamer`](StreamerRegistry.IStreamer.md)

## Implemented by

- [`PlayerConnection`](../classes/PlayerConnection.PlayerConnection.md)
- [`SFUConnection`](../classes/SFUConnection.SFUConnection.md)
- [`StreamerConnection`](../classes/StreamerConnection.StreamerConnection.md)

## Table of contents

### Methods

- [getReadableIdentifier](LoggingUtils.IMessageLogger.md#getreadableidentifier)

## Methods

### getReadableIdentifier

▸ **getReadableIdentifier**(): `string`

#### Returns

`string`

#### Defined in

[Signalling/src/LoggingUtils.ts:18](https://github.com/mcottontensor/PixelStreamingInfrastructure/blob/709d6fe/Signalling/src/LoggingUtils.ts#L18)
