# guixsh

_Run a shell or command inside a Guix profile_

**Note** I wrote _guixsh_ before Guix got environment and container support,
but still use it because it simple and effective.  `guix environment` may be
the better tool for the job now.

## guixsh

`guixsh` is a quick and simple way to start a 'pure' Guix shell, i.e. a shell
with no references to the host `PATH`, and in which only binaries installed
in the Guix profile are present.

Full documentation is in `guixsh --help`.

## .guixshrc

Script sourced by `guixsh` when it starts, as documentated in `guixsh --help`.
See `sample-guixsh` for an example.

## unguixsh

The _unguixsh_ script does the inverse of `guixsh`: it opens a shell in the
host environment from a guixsh.  The spawned shell has its PATH and environment
'reset' to host settings.  (Note: just a coarse hack.)

