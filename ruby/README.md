# Ruby


## RuboCop

We use RuboCop https://github.com/bbatsov/rubocop
> A Ruby static code analyzer, based on the community Ruby style guide

Our shared rubocop configs can be inherited from like this.
`.rubocop.yml`
```yaml
inherit_from:
  - https://raw.githubusercontent.com/apoex/styleguide/master/ruby/rubocop.yml
  - https://raw.githubusercontent.com/apoex/styleguide/master/ruby/rails_rubocop.yml

AllCops:
  TargetRubyVersion: 2.4
```
Certain things like `TargetRubyVersion` are best kept in `.rubocop.yml` for each
app.

When you run `rubocop` it will download and create a file for each of these
inheritances. We've found it best to check these files in to git.

Because having them ignored by git and fetched on demand did not work out of the
box with code climate.
