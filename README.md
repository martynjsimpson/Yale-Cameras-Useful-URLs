# Integrating Yale Smart Cameras

## Prerequisites

1. Username = The username for the camera, normally admin
2. Password = The xxx password set
3. IP = Address

## How to Use

This guide provides useful information about Yale Cameras for integrating with platforms like Home Assistant, OpenHab and others.

Variables are shown in { } and should be replaced (including the braces) with your own values. E.g {password} should be replaced with abc123 (assuming your password is abc123).

## Yale SV-DFFI-W Indoor Camera

| Platform | Type                        | Value                                        |
| -------- | --------------------------- | -------------------------------------------- |
| All      | Still image URL             | xxxx                                         |
| All      | Stream source URL           | rtsp://{username}:{password}@{ipaddress}:554 |
| HA       | RTSP transport protocol     | TCP                                          |
| HA       | Authentication              | digest                                       |
| HA       | Username                    | {username}                                   |
| HA       | Password                    | {password}                                   |
| HA       | Frame rate (Hz)             | 2                                            |
| HA       | Verify SSL certificate      | FALSE                                        |
| HA       | Limit refetch to URL change | FALSE                                        |

## Yale SV-DAFX-W Outdoor Camera

| Platform | Type                        | Value                                                                            |
| -------- | --------------------------- | -------------------------------------------------------------------------------- |
| All      | Still image URL             | http://{ipaddress}/cgi-bin/snapshot.cgi?chn=0&u={username}&p={password}          |
| All      | Stream source URL           | rtsp://{username}:{password}@{ipaddress}:554/cam/realmonitor?channel=1&subtype=0 |
| HA       | RTSP transport protocol     | TCP                                                                              |
| HA       | Authentication              | digest                                                                           |
| HA       | Username                    | {username}                                                                       |
| HA       | Password                    | {password}                                                                       |
| HA       | Frame rate (Hz)             | 2                                                                                |
| HA       | Verify SSL certificate      | FALSE                                                                            |
| HA       | Limit refetch to URL change | FALSE                                                                            |
