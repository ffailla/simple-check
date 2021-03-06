# Changelog

* 0.4.0
    * tuple generator now creates tuple types (from `clj-tuple`)
        * __BACKWARD_INCOMPATIBILITY__: `gen/tuple` now takes var-args, instead
        of a vector of arguments. So change:

        ```clojure
        (gen/tuple [gen/int gen/boolean])
        ```

        to

        ```clojure
        (gen/tuple gen/int gen/boolean)
        ```

        Tuples will now retain their size when shrunk.

    * add a `ratio` generator
    * correctly shrink empty lists
    * switch to `codox-md` for documentation

* 0.3.0
    * add strictly-positive and strictly-negative integer generators
    * allow scientific notation in number of tests parameter
    * allow specification of number of elements in vector generator

* 0.2.1
    * remove unused `diff` function
    * eliminate reflection warnings

* 0.2.0
    * added `gen/byte` and `gen/bytes`
    * swapped order of args in `gen/such-that`
    * swapped order of args in `simple-check.clojure-test/defspec`
    * add implicit `do` to `defspec` body

* 0.1.0
    * First release
