# IDR submission ticketing system

This is an email ticketing system for handling IDR data submissions.
The primary aim is to manage multiple complex email threads concerning data submissions to the IDR.

## Requirements

- All emails should be visible by the OME team
- Any member of the public should be able to email the system
- Emails may contain confidential information and must not be visible to others
- Emails should be sent and received via a dedicated email address
- OME team members email addresses should not be visible to data submitters

## Deployment

This application is deployed on Kubernetes using the manifests in [k8s](k8s).
To run this yourself add your postgres and GMail credentials to [k8s/secret-config.yaml.example](secret-config.yaml.example), and change [k8s/pv-nfs.yml](pv-nfs.yml) to point to a persistent volume.

## Issues to be discussed

- Should submitters have a login to the system, or should everything be done by email only?
- Should the quoted section of email replies be discarded (works if everyone top-posts, fails if replies are bottom-posted or in-line)
