# mu-image-testdata

Test fixtures (DNG files, comparison outputs) for the **public** mu-image project.

## Structure

```
mu-image-testdata/
├── dngtestfiles/          # DNG test files for muimg tests
├── output_comparison/     # Generated comparison outputs (gitignored)
└── README.md
```

## Usage

This repo is automatically cloned by test code when running tests in `mu-image`.

The test `conftest.py` will:
1. Check if `fixtures/` directory exists in the test folder
2. Clone this repo on first test run if not present
3. Tests then reference files via the fixtures path

## Manual Clone

If you need to clone manually:

```bash
cd /path/to/mu-image/muimg/tests
git clone git@github.com:mu-files/mu-image-testdata.git fixtures
```
