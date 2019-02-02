## Word Search System GRPC
Refer to general documentation here: https://github.com/chrisjpalmer/word_search

## Using this repository
### Compile
If you update the protocol buffers, you must rebuild the compiled golang source:
```sh
protoc -I ./ ./word_search_system_grpc.proto --go_out=plugins=grpc:./
dep ensure # Make sure the dependency tree is good
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
Someone should establish some versioning rules about when to change major, minor and patch values based on what changes in the protocol implementation.
For instance, removing fields is quite serious so that should probably be a breaking change. However adding fields might be a minor change.
