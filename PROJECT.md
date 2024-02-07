# Jagaad PHP Test Case

## 1- Create a cli command

We have two api that give us a list of users. We need a cli command that will fetch users from those endpoints and save user information into a csv file.

## 2- Create a cli command for searching users who has specific tags

We need a command for searching users that have specific tags inside the created csv file (see first item). Tags should be given via flag (like - - tag=sometag,anothertag). Users must have all given tags. When a user is found with given tags, its name and salary should be written on the output as a list.

### Endpoints

First api that needs to be hit
[https://run.mocky.io/v3/03d2a7bd-f12f-4275-9e9a-84e41f9c2aae](https://run.mocky.io/v3/63bdf98c-0fa8-4d6f-bce1-9a396291391a) (if this link is broken please let me know. Also you can find this response in `docs/error.json`)

Method: GET

Query string: ?verbose=1

(Yes, we know it gives 500 error, please handle the situation)


Second api

Method: GET

Query String: ?expose=1

[https://run.mocky.io/v3/aab281fe-3dbb-4d91-a863-a96e6bf083d7](https://run.mocky.io/v3/be735969-aba0-4f00-97bc-b40b4ae55f31) (if this link is broken please let me know. Also you can find this response in `docs/success.json`)

**Very Important Note**: These api urls look similar but, please consider these two endpoints as two different providers.

### Requirements;
- Using latest version of golang is important
- Having tests is important
