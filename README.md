
# website for the course GEO1101

## To compile locally

1. install the [Rust compiler](https://www.rust-lang.org/tools/install)
2. in the console: `cargo install mdbook`
3. those extensions of mdbook should be installed:
   1. `cargo install mdbook-admonish` (https://github.com/tommilligan/mdbook-admonish)
   1. `cargo install mdbook-hide` (https://github.com/ankitrgadiya/mdbook-hide/)
   1. `cargo install mdbook-image-size` <(https://github.com/lhybdv/mdbook-image-size)
   1. `cargo install mdbook-toc`

## To compile on-the-fly 

1. `mdbook serve`
2. open your browser at the URL given

## To build

`mdbook build`
