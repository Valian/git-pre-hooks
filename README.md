# git-pre-hooks
Automatic pre-commit quality checks example for [my blog post](https://rock-it.pl/automatic-code-quality-checks-with-git-hooks).
Basically, it's an example how to create pre-commit / pre-push hooks to automatically run tests.

## Other tools
Since writing this post, I've found a much better tool for running pre-commit hooks, called simply [pre-commit](https://pre-commit.com/). You should check it, as it's much more powerful and also easy to use.

## Short version

``` bash
git clone https://github.com/Valian/git-pre-hooks
cd git-pre-hooks
./scripts/install-hooks.bash

# now change something, and try to commit
echo "change!" >> README.md
git commit -am "test change"
>> Running pre-commit hook
>> Running tests
>> ............................
>> Failed!
>> Tests must pass before commit!
```

Actually tests are always failing, but you can easily adapt them to your use case. Skipping hook flag:

``` bash
git commit --no-verify
```

That's all. Leave a star if it helped you!
