Box Deployments
===============

This is a BOSH deployment repo, similar to [bosh-deployment ][1]
and [cf-deployment][2], but much reduced in scope, for testing and
other nefarious purposes.

To deploy it:

    bosh -d box deploy box.yml

To rename the deployment:

    bosh -d other-box deploy box.yml \
         -o ops/rename.yml \
         -v name=other-box

To scale up the number of boxen:

    bosh deploy box.yml \
         -o ops/scale.yml \
         -v instances=4

If you want a custom password:

    bosh deploy box.yml \
      -o ops/password.yml

etc.

It does, well, nothing.  But it does it well!

[1]: https://github.com/cloudfoundry/bosh-deployment
[2]: https://github.com/cloudfoundry/cf-deployment
