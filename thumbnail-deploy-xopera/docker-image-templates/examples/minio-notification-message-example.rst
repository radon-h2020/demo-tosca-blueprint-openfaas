MinIO notification message example
===================================

This is a template example of a JSON message sent to function by MinIO notification trigger.

.. code-block:: json

    {
      "EventName": "s3:ObjectCreated:Put",
      "Records": [
        {
          "s3": {
            "configurationId": "Config",
            "object": {
              "versionId": "1",
              "key": "image.jpg",
              "sequencer": "15CFEDF8D5304D1A",
              "contentType": "image/jpeg",
              "size": 224662,
              "userMetadata": {
                "content-type": "image/jpeg"
              },
              "eTag": "5fc7298143efe1276d39a3466d4e255f-1"
            },
            "s3SchemaVersion": "1.0",
            "bucket": {
              "ownerIdentity": {
                "principalId": "AKIAIOSFODNN7EXAMPLE"
              },
              "name": "bucket",
              "arn": "arn:aws:s3:::bucket"
            }
          },
          "eventSource": "minio:s3",
          "responseElements": {
            "x-amz-request-id": "15CFEDF8D4736ED9",
            "x-minio-origin-endpoint": "http://192.0.2.0:9000",
            "x-minio-deployment-id": "0170a4cc-dca6-4e72-86f1-c0cc760dff7f"
          },
          "source": {
            "userAgent": "Mozilla/5.0 (X11; Linux x86_64; rv:69.0) Gecko/20100101 Firefox/69.0",
            "port": "",
            "host": "192.0.2.0"
          },
          "eventName": "s3:ObjectCreated:Put",
          "userIdentity": {
            "principalId": "AKIAIOSFODNN7EXAMPLE"
          },
          "requestParameters": {
            "region": "",
            "sourceIPAddress": "192.0.2.0",
            "accessKey": "AKIAIOSFODNN7EXAMPLE"
          },
          "eventTime": "2019-10-22T09:27:27Z",
          "awsRegion": "",
          "eventVersion": "2.0"
        }
      ],
      "Key": "bucket/image.jpg"
    }
