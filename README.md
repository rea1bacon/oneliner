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