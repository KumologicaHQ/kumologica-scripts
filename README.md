# kumologica-scripts
Scripts required by kumologica designer and cli to interact with third party platforms (aws)

The following scripts are present:

## kumologica-designer.yaml

Script creates cloudformation stack that contains named policy that needs to be assigned to user.

To create stack run following command:

```bash
aws cloudformation create-stack \
    --stack-name kumologica-designer-stack  \
    --template-body file://kumologica-designer.yaml \
    --capabilities CAPABILITY_AUTO_EXPAND CAPABILITY_NAMED_IAM
```

To update stack run following command:

```bash
aws cloudformation update-stack \
    --stack-name kumologica-designer-stack  \
    --template-body file://kumologica-designer.yaml \
    --capabilities CAPABILITY_AUTO_EXPAND CAPABILITY_NAMED_IAM
```

The account the script runs must have cloudformation create and update stack permissions as well as create/update iam policy.