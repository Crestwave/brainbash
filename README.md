# brainbash

A brainfuck interpreter written in pure Bash

```bash
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
	- If there are no arguments, it reads from `/dev/tty`
- It only depends on Bash 4+ and is designed to be portable
- It does not optimize on specific patterns
- Unmatched brackets are only detected during runtime for speed

## Implementation Info

- Cells are 8-bit
- Cells wrap on overflow and underflow
- The cell is left unchanged on EOF
- The host's native character set is used (untested)
- Negative pointers are allowed
- Input is line buffered
