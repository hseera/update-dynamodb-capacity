# update dynamodb capacity
There might be cases in non-prod environment where you have lots of DynamoDB tables and each one either set to Provisioned or On-Demand capacity. If not properly managed, cost ($$) of keeping tables on Provisionsed capacity can escalate pretty quickly. 
This simple python script goes through all the tables and if they are running with provisioned capacity changes them to On-demand. If they are alread on On-Demand capacity, it doesn't nothing to those tables.
 

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
Once above prequisites are setup, execute the python script
```

## Improvements

* Check when was the table last changed to On-Demand capacity. If it was less than 24 hours than reduce the Provisioned capacity else change it to On-Demand.
* Improve on the get() function call. In future if AWS changes the json structure, this call if fail. Need to come up with a better approach. 
## Authors

* **Harinder Seera** - *Initial work* - [OzPerf](https://ozperf.com/)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

