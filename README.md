Forked from (https://github.com/danielgindi/express-compression/tree/feature/brotli)[https://github.com/danielgindi/express-compression/tree/feature/brotli]

Override the compression negotiation to always use the `br` encoding.


##### params - [key-value object containing indexed Brotli parameters](https://nodejs.org/api/zlib.html#zlib_brotli_constants)

  - `zlib.constants.BROTLI_PARAM_MODE`
    - `zlib.constants.BROTLI_MODE_GENERIC` (default)
    - `zlib.constants.BROTLI_MODE_TEXT`, adjusted for UTF-8 text
    - `zlib.constants.BROTLI_MODE_FONT`, adjusted for WOFF 2.0 fonts
  - `zlib.constants.BROTLI_PARAM_QUALITY`
    - Ranges from `zlib.constants.BROTLI_MIN_QUALITY` to
      `zlib.constants.BROTLI_MAX_QUALITY`, with a default of
      `4` (which is not node's default but the most optimal).

Note that here the default is set to compression level 4. This is a balanced setting with a very good speed and a very good
compression ratio.

