# Promtool docker action
This action executes `promtool` with the given arguments.

## Inputs
### `args`
The arguments to pass to `promtool`

## Example usage
```yml
on: [push]
jobs:
    test-alert-rules:
    runs-on: ubuntu-18.04
    steps:
    - name: 'Checkout'
      uses: 'actions/checkout@v2'
    - name: 'Run promtool tests'
      uses: 'MatsuriJapon/promtool-action@v1'
      with:
        args: 'test rules $(find monitoring/test -name *.yaml)
```
