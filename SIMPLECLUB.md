# simpleclub fork

Temporary fork of ory/terraform-provider-ory for simpleclub/infrastructure.

Branch `simpleclub` = upstream `main` + ory/terraform-provider-ory#431, which adds
`claims_source` and `requested_claims` to `ory_social_provider`. Without them, every
update of a social provider drops `claims_source` from the live provider.

The simpleclub Atlantis image builds this branch into a Terraform filesystem mirror
under the address `registry.terraform.io/ory/ory` (see `atlantis/Dockerfile` in
simpleclub/infrastructure).

Remove this fork when an upstream release contains both #429 (`subject_source`)
and #431 or #432 (`claims_source`). Then pin that release in simpleclub/infrastructure,
remove the mirror from the Atlantis image and archive this repository.
