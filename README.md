The very useful [trentm/json command](https://github.com/trentm/json) in a docker container.

This useful for environment where you can't install anything but dockers like [CoreOS](https://coreos.com/).

## Usage

```bash
$ docker pull jfromaniello/json
$ alias json="docker run -i --rm jfromaniello/json"
```

Then you can use the command as always:

```bash
$ echo '{"foo":"bar"}' | json
{
  "foo": "bar"
}

$ echo '{"foo":"bar"}' | json foo
bar

$ echo '{"age":10}' | json -E 'this.age++'
{
  "age": 11
}
```

## License

MIT 2014 - José F. Romaniello