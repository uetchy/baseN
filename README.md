# baseN

Create your ever dreamed baseN (N ⊂ 2^n) serialization algorithm.

## Usage

`python3 ./baseN.py --help`: show help

### Encode

```bash
python3 ./baseN.py <source text> --map <mapfile>
python3 ./baseN.py "Hello, world" --map ./maps/base64.map
```

the output should be:

```
Base64 (mapsize: 64)
source: Hello, world
target: SGVsbG8sIHdvcmxkA=
```

### Decode

```bash
python3 ./baseN.py <source text> --map <mapfile> --decode
python3 ./baseN.py "SGVsbG8sIHdvcmxkA=" --map ./maps/base64.map --decode
```

the output should be:

```
Base64 (mapsize: 64)
source: SGVsbG8sIHdvcmxkA=
target: Hello, world
```

### Custom map file

Your map file should contain `2^n` of arbitorary characters.

```bash
python3 ./baseN.py "Hello, world" --map ./maps/base256.map
```

the output should be:

```
Base256 (mapsize: 256)
source: Hello, world
target: けよををぎsgぞぎごをゆA=
```
