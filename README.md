# brainbash

A brainfuck interpreter written in pure Bash

```shell
$ brainbash examples/numwarp.b
123
    /\
     /\
  /\  /
   / 
 \ \/
  \
   
```

## Program Info

- It reads from a file named in the first argument
	- If there are no arguments, it reads from standard input
- It only depends on Bash 4+ and is designed to be portable
- It does not optimize on specific patterns
- Unmatched brackets are detected during runtime

## Implementation Info

- Cells are 8-bit
- Cells wrap on overflow and underflow
- The cell is left unchanged on EOF
- The host's native character set is used (untested)
- Negative pointers are allowed
- Input is line buffered

## Why?

I tried numerous interpreters and none of them were able to run all the example programs. So I decided to make one myself, implementing what I thought made sense, and it ended up being able to run every single program I tried.

It's not terribly fast, but I actually prefer it not to be instant; programs like Fibonacci are unreadable at faster speeds, and it's quick enough on my machine that I do not have any desire for it to be faster.
