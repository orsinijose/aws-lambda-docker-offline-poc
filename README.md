### README.

This POC runs a Hello World AWS lambda function locally using **[docker-lambda](https://github.com/lambci/docker-lambda)** project.

### Run

```
docker run --rm -v "$PWD":/var/task lambci/lambda:nodejs10.x index.handler '{"name": "event"}'
```

### Output

```
START RequestId: 52fdfc07-2182-154f-163f-5f0f9a621d72 Version: $LATEST
2019-07-26T13:41:49.404Z        52fdfc07-2182-154f-163f-5f0f9a621d72    INFO    { name: 'event' }
END RequestId: 52fdfc07-2182-154f-163f-5f0f9a621d72
REPORT RequestId: 52fdfc07-2182-154f-163f-5f0f9a621d72  Duration: 23.64 ms      Billed Duration: 100 ms Memory Size: 1536 MB    Max Memory Used: 44 MB
"hello event"
```

### To Do

- Test with existing Lambda functions.
- Check integration with other AWS resources (S3, SSM, Aurora RDS, IAM).
