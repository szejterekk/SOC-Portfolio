# Splunk Basics

## What is Splunk?

Splunk is a platform used to collect, search and analyze logs and security data.

In a SOC, analysts use Splunk to investigate alerts and suspicious activity.

## Architecture

Forwarder → collects and forwards data

Indexer → stores and processes data

Search Head → used to search and analyze data

## Events & Fields

Event = individual piece of ingested data.

Fields = useful information extracted from an event.

Examples:
user
src_ip
dest_ip
action
status
_time

## Indexes

An index stores events.

Example:

index=VPN_Logs

## Source & Sourcetype

source → where the data came from

sourcetype → what type of data it is

## Basic SPL

### Search an index:

index=VPN_Logs


### Filter by field:

index=VPN_Logs user="john"


### Filter by IP:

index=VPN_Logs src_ip="10.10.10.10"


### Count events:

index=VPN_Logs
| stats count

### Count by user:

index=VPN_Logs
| stats count by user

## SOC Workflow
```text
Alert
  ↓
Find relevant data
  ↓
Identify index
  ↓
Search events
  ↓
Filter fields
  ↓
Analyze activity
  ↓
Decide whether further investigation is needed
```
