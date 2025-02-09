[**@epicgames-ps/lib-pixelstreamingcommon-ue5.5**](../../../README.md)

***

[@epicgames-ps/lib-pixelstreamingcommon-ue5.5](../../../README.md) / [Logger/Logger](../README.md) / LoggerContext

# Class: LoggerContext

The global context for the logger configuration.
This cannot be stored statically in the Logger class because we sometimes have multiple execution
contexts, such as stats reporting. Instead we store the logger config context on the window object
to be shared with any Logger instances.

## Constructors

### new LoggerContext()

> **new LoggerContext**(): [`LoggerContext`](LoggerContext.md)

#### Returns

[`LoggerContext`](LoggerContext.md)

## Properties

### includeStack

> **includeStack**: `boolean` = `true`

#### Defined in

[Logger/Logger.ts:25](https://github.com/mcottontensor/PixelStreamingInfrastructure/blob/80aa060d880a8c194a04b83f18bd1ee360ab20e1/Common/src/Logger/Logger.ts#L25)

***

### logLevel

> **logLevel**: [`LogLevel`](../enumerations/LogLevel.md) = `LogLevel.Debug`

#### Defined in

[Logger/Logger.ts:24](https://github.com/mcottontensor/PixelStreamingInfrastructure/blob/80aa060d880a8c194a04b83f18bd1ee360ab20e1/Common/src/Logger/Logger.ts#L24)
