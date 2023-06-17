# enum_data_proc
Add bit operations and arithmetic operations to enum

# example

```rust
use enum_data_proc::*;

#[repr(u32)]
#[derive(BitOp,ArithOp)]
enum A{
    a=7,b,c,d,e,f,
}

fn main() {
    println!("{:?}",[
        A::a+1,
        A::b<<1,
        1&A::c,
        A::d|A::d,
        A::e%2,
        2*A::f]
    );
}

```