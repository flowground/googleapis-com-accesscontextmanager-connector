# ![LOGO](logo.png) Access Context Manager **flow**ground Connector

## Description

A generated **flow**ground connector for the Access Context Manager API (version v1beta).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/accesscontextmanager/v1beta/swagger.json<br/>
Generated at: 2019-05-07T17:41:04+03:00

## API Description

An API for setting attribute based access control to requests to GCP services.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### List all AccessPolicies under a<br/>
> container.

*Tags:* `accessPolicies`

#### Input Parameters
* `pageSize` - _optional_ - Number of AccessPolicy instances to include in the list. Default 100.
* `pageToken` - _optional_ - Next page token for the next batch of AccessPolicy instances. Defaults to
the first page of results.
* `parent` - _optional_ - Required. Resource name for the container to list AccessPolicy instances
from.

Format:
`organizations/{org_id}`
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Create an `AccessPolicy`. Fails if this organization already has a<br/>
> `AccessPolicy`. The longrunning Operation will have a successful status<br/>
> once the `AccessPolicy` has propagated to long-lasting storage.<br/>
> Syntactic and basic semantic errors will be returned in `metadata` as a<br/>
> BadRequest proto.

*Tags:* `accessPolicies`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Delete an Access Level by resource<br/>
> name. The longrunning operation from this RPC will have a successful status<br/>
> once the Access Level has been removed<br/>
> from long-lasting storage.

*Tags:* `accessPolicies`

#### Input Parameters
* `name` - _required_ - Required. Resource name for the Access Level.

Format:
`accessPolicies/{policy_id}/accessLevels/{access_level_id}`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Get an Access Level by resource<br/>
> name.

*Tags:* `accessPolicies`

#### Input Parameters
* `accessLevelFormat` - _optional_ - Whether to return `BasicLevels` in the Cloud Common Expression
Language rather than as `BasicLevels`. Defaults to AS_DEFINED, where
Access Levels
are returned as `BasicLevels` or `CustomLevels` based on how they were
created. If set to CEL, all Access Levels are returned as
`CustomLevels`. In the CEL case, `BasicLevels` are translated to equivalent
`CustomLevels`.
    Possible values: LEVEL_FORMAT_UNSPECIFIED, AS_DEFINED, CEL.
* `name` - _required_ - Required. Resource name for the Access Level.

Format:
`accessPolicies/{policy_id}/accessLevels/{access_level_id}`
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Update an Access Level. The longrunning<br/>
> operation from this RPC will have a successful status once the changes to<br/>
> the Access Level have propagated<br/>
> to long-lasting storage. Access Levels containing<br/>
> errors will result in an error response for the first error encountered.

*Tags:* `accessPolicies`

#### Input Parameters
* `name` - _required_ - Required. Resource name for the Access Level. The `short_name` component
must begin with a letter and only include alphanumeric and '_'. Format:
`accessPolicies/{policy_id}/accessLevels/{short_name}`
* `updateMask` - _optional_ - Required.  Mask to control which fields get updated. Must be non-empty.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### List all Access Levels for an access<br/>
> policy.

*Tags:* `accessPolicies`

#### Input Parameters
* `accessLevelFormat` - _optional_ - Whether to return `BasicLevels` in the Cloud Common Expression language, as
`CustomLevels`, rather than as `BasicLevels`. Defaults to returning
`AccessLevels` in the format they were defined.
    Possible values: LEVEL_FORMAT_UNSPECIFIED, AS_DEFINED, CEL.
* `pageSize` - _optional_ - Number of Access Levels to include in
the list. Default 100.
* `pageToken` - _optional_ - Next page token for the next batch of Access Level instances.
Defaults to the first page of results.
* `parent` - _required_ - Required. Resource name for the access policy to list Access Levels from.

Format:
`accessPolicies/{policy_id}`
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Create an Access Level. The longrunning<br/>
> operation from this RPC will have a successful status once the Access<br/>
> Level has<br/>
> propagated to long-lasting storage. Access Levels containing<br/>
> errors will result in an error response for the first error encountered.

*Tags:* `accessPolicies`

#### Input Parameters
* `parent` - _required_ - Required. Resource name for the access policy which owns this Access
Level.

Format: `accessPolicies/{policy_id}`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### List all Service Perimeters for an<br/>
> access policy.

*Tags:* `accessPolicies`

#### Input Parameters
* `pageSize` - _optional_ - Number of Service Perimeters to include
in the list. Default 100.
* `pageToken` - _optional_ - Next page token for the next batch of Service Perimeter instances.
Defaults to the first page of results.
* `parent` - _required_ - Required. Resource name for the access policy to list Service Perimeters from.

Format:
`accessPolicies/{policy_id}`
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Create an Service Perimeter. The<br/>
> longrunning operation from this RPC will have a successful status once the<br/>
> Service Perimeter has<br/>
> propagated to long-lasting storage. Service Perimeters containing<br/>
> errors will result in an error response for the first error encountered.

*Tags:* `accessPolicies`

#### Input Parameters
* `parent` - _required_ - Required. Resource name for the access policy which owns this Service
Perimeter.

Format: `accessPolicies/{policy_id}`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-accesscontextmanager-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
