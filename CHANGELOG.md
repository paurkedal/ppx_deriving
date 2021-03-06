Changelog
=========

2.1
---

  * Fix prefixed attribute names ([@deriving.foo.attr] and [@foo.attr]).

2.0
---

  * Add support for open types.

1.1
---

  * New plugin: create.
  * Show, eq, ord: handle `_`.
  * Show, eq, ord, map, iter, fold: handle inheriting from a parametric
    polymorphic variant type.
  * Make Ppx_deriving.poly_{fun,arrow}_of_type_decl construct functions
    in correct order. This also fixes all derivers with types with
    more than one parameter.
  * Add Ppx_deriving.fold_{left,right}_type_decl.

1.0
---

  * Make deriver names lowercase.
  * Remove Findlib+dynlink integration. All derivers must now be
    explicitly required.
  * Allow shortening [%derive.x:] to [%x:] when deriver x exists.
  * Make Ppx_deriving.core_type field optional to allow ignoring
    unsupported [%x:] shorthands.
  * Add support for [@@deriving foo { optional = true }] that does
    not error out if foo is missing, useful for optional dependencies.
  * Rename ~name and ~prefix of Ppx_deriving.attr and
    Ppx_deriving.Arg.payload to ~deriver.
  * Renamed Ppx_deriving.Arg.payload to get_attr.
  * Add Ppx_deriving.Arg.get_expr and get_flag.

0.3
---

  * Show, Eq, Ord, Iter, Fold: handle ref.
  * Show: handle functions.
  * Show: include break hints in format strings.
  * Show: pull fprintf into local environment.
  * Show: add [@polyprinter] and [@opaque].
  * Add Ppx_deriving.Arg.expr.

0.2
---

  * New plugins: Enum, Iter, Map, Fold.
  * All plugins: don't concatenate affix if type is named `t`.
  * Add [%derive.Foo:] shorthand.
  * Show, Eq, Ord: add support for list, array, option.
  * Show: include full module path in output, including for types with manifest.
  * A lot of changes in Ppx_deriving interface.

0.1
---

  * Initial release.
