# Case-insensitive comparison: implementation

## What the example does

Casefold is stronger than lower: German sharp-s expands to ss. Normalize Unicode separately when canonical equivalence matters.

The public function is `solve(value)`. The JSON input contract can be seen in this concrete example:

```json
[
  "Straße",
  "STRASSE"
]
```

Expected result:

```json
true
```

Run `python3 example.py` for the Python representation of the result. `solution.py` contains the full implementation and can also be imported by another script.

## Scope

The function implements exactly the behavior described above. It does not perform network or filesystem access. Python exceptions indicate unsupported input; the next lesson turns them into a command-line error response. Review the limitations before reusing it in an application.
