# sml-uri
Library for URIs in Standard ML, designed for the
[smlpkg](https://github.com/diku-dk/smlpkg) package manager. The library
provides a single structure, `URI`, as documented below.

## Library sources

`lib/github.com/shwestrick/sml-uri/uri.mlb`

## Interface

```sml
structure URI :>
sig
  type t
  type uri = t

  val fromString: string -> uri
  val toString: uri -> string

  val scheme: uri -> string
  val authority: uri -> string option
  val path: uri -> string
  val query: uri -> string option
  val fragment: uri -> string option

  val make:
    { scheme: string
    , authority: string option
    , path: string
    , query: string option
    , fragment: string option
    }
    -> uri
end
```
