# gitlab-ci-templates

## A collection of `.gitlab-ci.yml` templates and includes for Security Products

This is Security Products collection of [`.gitlab-ci.yml`][ci-docs] file templates,
to be used in conjunction with [GitLab CI][gl-ci].

For more information about how `.gitlab-ci.yml` files work, and how to use them,
please read the [documentation on GitLab CI][ci-docs]. Please keep in mind that
these templates might need editing to suit your setup, and should be considered
guideline.

[ci-docs]: http://docs.gitlab.com/ce/ci/
[gl-ci]: https://about.gitlab.com/gitlab-ci/


To make runner run, then add the following tag: `security`


include:remote
include:remote can be used to include a file from a different location, using HTTP/HTTPS, referenced by using the full URL. The remote file must be publicly accessible through a simple GET request as authentication schemas in the remote URL is not supported. For example:

```
include:
  - remote: 'https://gitlab.com/awesome-project/raw/master/.gitlab-ci-template.yml'
```

All nested includes will be executed without context as public user, so only another remote, or public project, or template is allowed.
