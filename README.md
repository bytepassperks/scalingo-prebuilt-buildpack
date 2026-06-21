# scalingo-prebuilt-slug-buildpack

A minimal Scalingo buildpack that decompresses a pre-built application slug
(`slug.tar.gz`) shipped in the deploy archive. Lets large pre-built apps
(>300MB extracted) deploy under Scalingo's archive-fetch cap by keeping the
heavy artifacts in a single compressed blob that is expanded at compile time.

Usage: set `BUILDPACK_URL` to this repo, ship an archive containing
`slug.tar.gz` + `Procfile`.
