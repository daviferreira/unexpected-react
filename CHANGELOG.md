# Changelog

## v0.2.x

Original version from [podio](https://github.com/podio)

## v0.3.0

Initial version using [unexpected-htmllike](https://github.com/bruderstein/unexpected-htmllike) and 
[react-render-hook](https://github.com/bruderstein/react-render-hook) to provide assertions on the 
full virtual DOm

## v0.3.1

Fix dependencies - issue seen when using npm 2.x (thanks to @faceyspacey for reporting)

## v0.3.2

Fix error handling when react-render-hook was not injected

## v0.4.0

Update to v0.4.1 of unexpected-htmllike-jsx-adapter, to add support for iterators as children
Thanks to @jkimbo for the failing test, and @Lugribossk for reporting

## v0.4.1

Force dependency update to unexpected-htmllike 0.3.2 - important bugfix for 'to contain', when a child element 
is not identical, but actually matches with the `to contain` flags that are in place.

## v0.5.0

Update to unexpected-htmllike 0.4.0, and add className diffing, using class semantics. i.e. order does not matter,
extra classes are ignored by default (not with `exactly` style assertions).

## v0.5.1

Patch version of unexpected-htmllike-jsx-adapter to support flattening children (only a package.json update)

## v0.5.2

Patch version of unexpected-htmllike to ^0.5.0 to fix issue with reordered children

## v1.0.0

Update to unexpected-htmllike v1.0.0 - much faster due to attempting everything sync first, before reverting  
to async if an async assertion is encountered.  You no longer need to return the result of the `expect`, unless 
you're actually doing an asynchronous `expect.it()` assertion somewhere in your `expected` value. 

## v1.0.1

Patch version of unexpected-htmllike to ^1.1.0 (improves output for function props, and props with undefined values - #15)

## v2.0.0

Props / Attributes are now tested with `to satisfy` semantics, unless `exactly` is specified, in which case
`to equal` is used.  This is probably what was expected, but could mean some tests that previously failed now pass,
hence the major version.

`queried for` support for both shallow and deep renderers
`with event` event triggering for shallow and deep renderers