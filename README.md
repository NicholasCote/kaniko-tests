# Running builds with Kaniko

## Create a secret file with Harbor URL and credentials

Use base64 encoding for the username & password used. 

`echo -n username:password | base64`

kubectl create secret generic -n ncote-test kaniko-config-json --from-file=config.json

## Apply the kaniko pod