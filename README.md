# BOSH Release for Debugging BOSH Deployments

## Purpose

This (very small) BOSH release dumps the some internal state /
information about a deployment into `/var/vcap/jobs/debug/...`,
including things like the Job spec (spec.yml) and the configured
properties (properties.yml).  This can be useful when developing
BOSH releases, or troubleshooting deployments to ensure that what
you are putting in the manifest is making it to the VMs.

**NOTE** due to some (recent?) changes to how BOSH handles the
properties given in the manifest, you now have to wrap the
job-level properties in another `properties` key.  The example
manifest (`manifests/debug.yml`) shows how.
