# dynamodb-billing-mode
Change DynamoDB capacity from Provisioned to On Demand.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

What things you need to execute the script

```
1: awscli
2: boto3
3: python 3.5
4: Setup your AWS Access, Secret key and the AWS region

```

### Execution

```
1: Once above prequisites are setup, execute the python script
```

## Improvements

* Check when was the table last changed to On-Demand capacity. If it was less than 24 hours than reduce the Provisioned capacity else change it to On-Demand.
## Authors

* **Harinder Seera** - *Initial work* - [OzPerf](https://ozperf.com/)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

