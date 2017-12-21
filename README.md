# Serverless Delete Loggroups
There are cases in which it is necessary to delete all log groups when upgrading to Serverless 1.6. This plugin can delete all log groups of the Lambda function described in serverless.yml

## Install

Run `npm install` in your Serverless project.

```
$ npm install serverless-delete-loggroups
```

Add the plugin to your serverless.yml file

```yaml
plugins:
  - serverless-delete-loggroups
```

Add additional extra log groups to delete

```yaml
custom:
    loggroups:
        extra: ["loggroup-name-1", "loggroup-name-2"]
```

## Command
LogGroups are deleted as follow:

```
$ sls remove logs
```

### options
- --stage or -s The stage in your service you want to delete.
- --region or -r The region in your stage that you want to delete.
