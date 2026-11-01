# Era Gzip (`github.com/era-lang-official/gzip`)

RFC 1952 Gzip compression container framing and IEEE 802.3 CRC-32 checksums for Era.

## Features
- **CRC-32**: Standard 32-bit cyclic redundancy check and hex representation.
- **Compression**: RFC 1952 Gzip file format packaging with CRC-32 and ISIZE verification.
- **Decompression**: Extracts payloads from Gzip wire buffers.

## Usage
```era
import "github.com/era-lang-official/gzip";

fn main() {
    let raw = "Hello world from Era".to_string();
    let gz = compress_gzip(raw.clone());
    let decompressed = decompress_gzip(gz).unwrap();
    println(decompressed); // "Hello world from Era"
}
```

