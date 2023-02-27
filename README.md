# Client-side encrypted backups of Talos etcd to AWS S3

This repo contains example Kubernetes CronJob manifests to backup the etcd state store of [Talos Linux](https://talos.dev/) to S3-compatible storage.

The approach uses the command-line tool [talosctl](https://www.talos.dev/v1.3/learn-more/talosctl/) and a dedicated Talos API account with limited privileges to create a snapshot file. The snapshot file is then encrypted client-side and backup up using [restic](https://restic.net/).

For full step-by-step instructions, please see my [blog post](https://alexlubbock.com/encrypted-backup-talos-etcd-aws-s3).