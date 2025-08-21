# Secure Checkout
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/n80fr1n60/hello-action/badge)](https://scorecard.dev/viewer/?uri=github.com/n80fr1n60/hello-action)
[![CI](https://github.com/n80fr1n60/hello-action/actions/workflows/build.yml/badge.svg)](https://github.com/n80fr1n60/hello-action/actions/workflows/build.yml)

A drop-in replacement for [actions/checkout](https://github.com/actions/checkout)  
that **always sets `persist-credentials: false`** for improved security.

## Why?
By default, `actions/checkout` persists the GitHub token in `.git/config`.  
This can unintentionally expose credentials to later steps or third-party actions.  
This action disables that by default, while keeping all other features intact.

## Usage

Replace:

```yaml
- uses: actions/checkout@v5
with 
- uses: n80fr1n60/secure-checkout@v1
