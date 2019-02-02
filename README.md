## Word Search System GRPC
This repository contains the protoc definitions for the word_search_system grpc standard.

## Using this repository
### Compile
If you update the protocol buffers, you must rebuild the compiled golang source:
```sh
protoc -I ./ ./word_search_system_grpc.proto --go_out=plugins=grpc:./
```

To do this you need to have protoc compiler installed. If you don't have this installed, follow these instructions: https://grpc.io/docs/quickstart/go.html

### Commit
Commit the changes, and increase the tag.
```sh
git commit -m 'commit message'
git tag X.X.X
git push; git push --tags
```

#### Commit Rules
- If you are removing fields from the protocol buffers, this is a breaking change and you must increase the major version number.
- If you are adding fields only, you may increase the minor version number.
- If you are changing a dependency to do with grpc, you must increase the patch version number.
