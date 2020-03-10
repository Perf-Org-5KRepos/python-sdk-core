[![Build Status](https://travis-ci.com/IBM/python-sdk-core.svg?branch=master)](https://travis-ci.com/IBM/python-sdk-core)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)[![codecov](https://codecov.io/gh/IBM/python-sdk-core/branch/master/graph/badge.svg)](https://codecov.io/gh/IBM/python-sdk-core)
[![Latest Stable Version](https://img.shields.io/pypi/v/ibm-cloud-sdk-core.svg)](https://pypi.python.org/pypi/ibm-cloud-sdk-core)
[![CLA assistant](https://cla-assistant.io/readme/badge/ibm/python-sdk-core)](https://cla-assistant.io/ibm/python-sdk-core)

# IBM Python SDK Core Version 1.7.1
This project contains core functionality required by Python code generated by the IBM Cloud OpenAPI SDK Generator
(openapi-sdkgen).

# Notice
Support for Python versions 2.x and versions <= 3.4 is deprecated and will be officially dropped in the next major release,
which is expected to be end of December, 2019.

## Installation

To install, use `pip` or `easy_install`:

```bash
pip install --upgrade ibm-cloud-sdk-core
```

or

```bash
easy_install --upgrade ibm-cloud-sdk-core
```

## Authentication
The python-sdk-core project supports the following types of authentication:
- Basic Authentication
- Bearer Token
- Identity and Access Management (IAM)
- Cloud Pak for Data
- No Authentication

For more information about the various authentication types and how to use them with your services, click [here](Authentication.md)

## Issues

If you encounter an issue with this project, you are welcome to submit a [bug report](https://github.com/IBM/python-sdk-core/issues).
Before opening a new issue, please search for similar issues. It's possible that someone has already reported it.

## Logging

### Enable logging

```python
import logging
logging.basicConfig(level=logging.DEBUG)
```

This would show output of the form:
```
DEBUG:urllib3.connectionpool:Starting new HTTPS connection (1): iam.cloud.ibm.com:443
DEBUG:urllib3.connectionpool:https://iam.cloud.ibm.com:443 "POST /identity/token HTTP/1.1" 200 1809
DEBUG:urllib3.connectionpool:Starting new HTTPS connection (1): gateway.watsonplatform.net:443
DEBUG:urllib3.connectionpool:https://gateway.watsonplatform.net:443 "POST /assistant/api/v1/workspaces?version=2018-07-10 HTTP/1.1" 201 None
DEBUG:urllib3.connectionpool:Starting new HTTPS connection (1): gateway.watsonplatform.net:443
DEBUG:urllib3.connectionpool:https://gateway.watsonplatform.net:443 "GET /assistant/api/v1/workspaces/883a2a44-eb5f-4b1a-96b0-32a90b475ea8?version=2018-07-10&export=true HTTP/1.1" 200 None
DEBUG:urllib3.connectionpool:Starting new HTTPS connection (1): gateway.watsonplatform.net:443
DEBUG:urllib3.connectionpool:https://gateway.watsonplatform.net:443 "DELETE /assistant/api/v1/workspaces/883a2a44-eb5f-4b1a-96b0-32a90b475ea8?version=2018-07-10 HTTP/1.1" 200 28
```

### Low level request and response dump
To get low level information of the requests/ responses:

```python
from http.client import HTTPConnection
HTTPConnection.debuglevel = 1
```

## Open source @ IBM

Find more open source projects on the [IBM Github Page](http://github.com/IBM)

## License

This library is licensed under Apache 2.0. Full license text is
available in [LICENSE](LICENSE).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).
