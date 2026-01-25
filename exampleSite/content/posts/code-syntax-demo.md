---
title: "Code Syntax Highlighting Demo"
date: 2026-01-25T11:00:00+08:00
draft: false
tags:
  - tutorial
  - code
categories:
  - development
---

Bat theme supports powerful code syntax highlighting with Dracula theme colors, making your code more readable.

## Supported Languages

The theme supports syntax highlighting for the following programming languages:

- JavaScript / TypeScript
- Python
- Go
- Rust
- Java
- C / C++
- HTML / CSS
- Ruby
- PHP
- Shell scripts
- And more...

## JavaScript Example

```javascript
// Functional programming example
const compose = (...fns) => (value) =>
  fns.reduceRight((acc, fn) => fn(acc), value);

// Function to calculate square
const square = (x) => x * x;

// Function to increment
const increment = (x) => x + 1;

// Compose functions
const squareThenIncrement = compose(increment, square);

// Usage
console.log(squareThenIncrement(5)); // 26
```

## Python Example

```python
# Class definition example
class Blog:
    """Blog class"""

    def __init__(self, title, author):
        self.title = title
        self.author = author
        self.posts = []

    def add_post(self, post):
        """Add a post"""
        self.posts.append(post)
        print(f"Post '{post}' added to '{self.title}'")

    def show_stats(self):
        """Show statistics"""
        print(f"Blog: {self.title}")
        print(f"Author: {self.author}")
        print(f"Posts: {len(self.posts)}")

# Usage
my_blog = Blog("Tech Blog", "John Doe")
my_blog.add_post("First Post")
my_blog.show_stats()
```

## Go Example

```go
// Concurrent processing example
package main

import (
    "fmt"
    "sync"
)

func main() {
    var wg sync.WaitGroup
    ch := make(chan int, 10)

    // Start multiple goroutines
    for i := 0; i < 5; i++ {
        wg.Add(1)
        go func(n int) {
            defer wg.Done()
            ch <- n * n
            fmt.Printf("Sent: %d\n", n*n)
        }(i)
    }

    // Wait for all goroutines to complete
    go func() {
        wg.Wait()
        close(ch)
    }()

    // Receive results
    for result := range ch {
        fmt.Printf("Received: %d\n", result)
    }
}
```

## Line Numbers

All code blocks display line numbers by default, making it easy to reference specific lines when writing tutorials or documentation.

## Custom Configuration

You can configure code highlighting in your `config.toml`:

```toml
[markup]
  [markup.highlight]
    style = "dracula"  # Theme
    lineNos = true      # Show line numbers
    lineNumbersInTable = false
```

## Mixed Languages

In Markdown, you can specify the language to get proper syntax highlighting:

``````python
def hello():
    print("Hello from Python!")
``````

``````javascript
function hello() {
    console.log("Hello from JavaScript!");
}
``````

Enjoy clean code display!
