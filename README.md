# Ruby Object Serializer

A small Ruby exercise that turns domain objects into nested hashes through a reusable serializer base class.

## Example

```ruby
post = Post.new(title: "Serialization", comments: [Comment.new(body: "Clear")])
PostSerializer.new(post).serialize
```

`Serializer` defines the shared attribute/association behavior. `PostSerializer` and `CommentSerializer` demonstrate scalar fields and nested collections without external serialization gems.

## Setup

```bash
bundle install
bundle exec rspec
```

The repository originated as a time-boxed interview exercise; that attribution and narrow scope are preserved. Specs cover the base serializer and both concrete serializers but were not run during the portfolio review. Circular references, conditional fields, key transforms, and large object graphs are outside the demonstrated implementation.
