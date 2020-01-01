# update dynamodb capacity
There might be cases when you end up having a lot of DynamoDB tables in your  non-prod environment and they might be either set to Provisioned or On-Demand capacity. If they are not properly managed, cost ($$) of keeping these tables on Provisioned capacity can escalate pretty quickly. This simple python script goes through all the tables and if they are on provisioned capacity changes them to On-demand. If they are already on On-Demand capacity, it doesn't nothing. 

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

If you would like to contribute to this project, please reachout to me.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

