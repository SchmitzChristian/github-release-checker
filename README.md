# github-release-checker

checks for a new release in a github repository. github-release-checker exists with exit code 1 if the given version differs compared to the latest release.

The target repository needs to tag their latest release for this CLI to work.

## example

```bash
$ docker run github-release-checker hashicorp/terraform v0.12.0
hashicorp/terraform version v0.12.24 is newer then v0.12.0
```

## Features

- ignore 'v' characters in version numbers (e.g. v1.2.3 = 1.2.3)
- able to ignore patch and minor version differences (--ignore-patch --ignore-minor)

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Developing

```bash
docker build . -t github-release-checker && docker run github-release-checker hashicorp/terraform 0.12.0
```

## License

[MIT](https://choosealicense.com/licenses/mit/)
