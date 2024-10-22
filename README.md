# `fetchTree` specification and conformance suite

`builtins.fetchTree` allows expressions in the Nix language to make use of files that reside in various places, such as other Git repositories.

The Nix expression language aims to be reproducible, so it follows that the behavior of `fetchTree` must be consistent between implementations, and consistent over time.

When this consistency is lost, you lose the ability to produce the same derivations, which in turns causes other problems such as an inability to use the existing contents of your binary cache for those derivations affected.

For these reasons it is crucial that we pin down the exact behavior of built-in fetchers, not just for a single Nix implementation, but in the wider Nix ecosystem.

# Work in progress

This repository aims to provide a specification and a conformance suite: files that can be used in implementations' test suites.

You are invited to collaborate.