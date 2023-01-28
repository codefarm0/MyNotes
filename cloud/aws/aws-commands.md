# AWS commands

## basics
* aws configure

## S3
* aws s3 mb s3://redshift-import-code-freeze
* aws s3api put-object --bucket redshift-import-code-freeze --key redshift-data.csv --body D:\greenlearner\experiments\aws\redshift-data.csv
* aws s3 ls s3://redshift-import-code-freeze

## dynamo DB
* create-table --table-name redshift-import --attribute-definitions AttributeName=ID,AttributeType=N --key-schema AttributeName=ID,KeyType=HASH --provisioned-throughput ReadCapacityUnits=5,WriteCapacityUnits=5

## Redshift
