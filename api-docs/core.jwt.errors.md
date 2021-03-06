<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@digitalpersona/core](./core.md) &gt; [JWT](./core.jwt.md) &gt; [errors](./core.jwt.errors.md)

## JWT.errors() method

Validates the JSON Web Token and returns a collection of detected validation errors.

<b>Signature:</b>

```typescript
static errors(jwt: JSONWebToken): Error[] | null;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  jwt | <code>JSONWebToken</code> | a JSON Web Token. |

<b>Returns:</b>

`Error[] | null`

an array of errors found, or `null` if the token is valid.

## Remarks

Only client-side checks are performed, no signature validation. The token's claims must satisfy following expression: `iat <= nbf < now < exp` where `iat` is time when the token was issued, `nbf` is a time when the token becomes valid, `exp` is a token expiration time, `now` is current time. Following errors may be returned:

\* 'JWT.Error.IssueTimeLaterThanNotBefore' if `iat > nbf`<!-- -->, \* 'JWT.Error.NotEffectiveYet' when `now < nbf`<!-- -->, \* 'JWT.Error.Expired' when `now >= exp`<!-- -->.

