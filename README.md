# Usefull oneliners to learn rust

---

```rust
fn solution(s: &str) -> Vec<String> {
    s.chars()
        .chain(std::iter::once('_'))
        .collect::<Vec<_>>()
        .chunks_exact(2)
        .map(|chunk| chunk.iter().collect())
        .collect()    
}
```

### Explanation

This one-liner splits the string into pairs of two characters. If the string contains an odd number of characters then it should replace the missing second character of the final pair with an underscore ('_').

It first convert the string to an iterator of chars. 
    
```rust
chain(std::iter::once('_')) 
``` 
Then it chains the iterator with an iterator of one char.

```rust
chunks_exact(2)
```

then it iterate over the vector and collect each pair of characters into a new vector.

```rust
map(|chunk| chunk.iter().collect())
```

Finally it collects every chunk into a new vector.


```rust
collect()
```
