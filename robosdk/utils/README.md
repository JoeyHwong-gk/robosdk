# utils

## fileops.py

- install dependent
 
```bash
pip3 install minio~=7.0.3 requests~=2.27.1
```

- test code

```python
import os
from robosdk.utils.fileops import FileOps

os.environ["S3_ENDPOINT_URL"] = '<your endpoint>'
os.environ["ACCESS_KEY_ID"] = '<your accesskey>'
os.environ["SECRET_ACCESS_KEY"] = '<your secretkey>'

FileOps.download("s3://test/sdk.png", "D:\\robotics\\robosdk\\docs\\image")  # download from s3
FileOps.upload("D:\\robotics\\robosdk\\docs\\image\\sdk.png", "s3://test/sdk.png")  #upload to s3

```
