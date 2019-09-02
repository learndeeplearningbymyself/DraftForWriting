# Dynamodb Stream

Reference from [source](https://qiita.com/Fujimon_fn/items/1f18360ee9ebf6832617)

## Definition

It is a function that can detect addition, change, and deletion of items to DynamoDB as events

By using DynamoDB Stream, when items are added or changed, a notification will be pushed. This time, we can get that events by **Lambda**

## Enable Stream on DynamoDB

Enable Stream from **Manage Streams** in DynamoDB Overview tab

<img src="" width="720">

## Required Permissions for Lambda to get events from DynamoDB Stream

It is necessary to grant the following four privileges to the stream of the table you want to read

- GetShardIterator
- GetRecords
- ListStream
- DescribeStream

## Add trigger of DynamoDB Stream from Lambda