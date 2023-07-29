Easily encode and decode bytes to send data over network

## Installation
Add to `Cargo.toml`
```
bytes_convert = "1.0.0"
```
To use the latest development version:
```
bytes_convert = { git = "https://github.com/positiveway/bytes_convert", branch = "main" }
```


## Usage
```
use bytes_convert::{to_bytes, from_bytes};

fn main() {
    let input_data = &[-2i16, -7, 9, 31];
    let converted_bytes = to_bytes(input_data);
    println!("{}", converted_bytes.len());

    //convert back to original data
    let original_data: Vec<i16> = from_bytes(converted_bytes);
    for item in &original_data {
        println!("{}", item)
    };
}
```