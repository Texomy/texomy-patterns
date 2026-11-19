# Texomy Patterns

Repository of reusable Texomy packages.

## Layout

Each package version lives at `<package path>/<version>/` with its own `texomy.json`:

```text
texomy/core/1.0.0/
  texomy.json        { "name": "texomy.core", "version": "1.0.0" }
  numbers.yml
  money.yml
  datetime.yml
  measurement.yml
```

A published version is never changed; changes go into a new version directory.

## Use

Declare this repository and the dependency in your project's `texomy.json`:

```json
{
  "repositories": { "texomy": "https://raw.githubusercontent.com/texomy/patterns/main/" },
  "dependencies": { "core": "texomy:texomy.core:1.0.0" }
}
```

Then import its specs by module name:

```yaml
$imports: [ core:money, core:datetime ]
```

## Legacy

`core/v1/` is the pre-package layout used by `$dependencies` URLs. It stays until clients move to the package layout.
