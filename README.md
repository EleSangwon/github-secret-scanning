# github-secret-scanning

This repo is a github secret scanning method using github action and [truffleHog3](https://github.com/feeltheajf/trufflehog3).

## A. Individual repo scanning

## Usage
[secret-scanning.yml](https://github.com/EleSangwon/github-secret-scanning/blob/master/.github/workflows/secret-scanning.yml)

```
When a PR or Push event occurs, secret scanning in the repo
```
## Result
![image](https://user-images.githubusercontent.com/50174803/191537038-5878881c-ff7e-4cdc-a866-30fa0a508628.png)
![image](https://user-images.githubusercontent.com/50174803/191537104-1e674d35-c0e1-410a-9394-352a300fda83.png)


## B. All repo secret scanning

## Usage
[all-repo-scan.yml](https://github.com/EleSangwon/github-secret-scanning/blob/master/.github/workflows/all-repo-scan.yml)

```
Read the repo-list.json file and scan all the repo in it
```

### how to get repo list

```
1. install ghcli https://cli.github.com/
2. gh repo list 
```
#### example 
```
gh repo list --json name --visibility public --source > public-repo-list.json
gh repo list --json name --visibility private --source > private-repo-list.json

```
![image](https://user-images.githubusercontent.com/50174803/191538362-b882f6f2-24da-416a-923a-b63eeac0cb88.png)

## Result
![image](https://user-images.githubusercontent.com/50174803/191538581-53886985-9e4c-4d6e-ae92-afd1b9c914f1.png)
[ Report ]
![image](https://user-images.githubusercontent.com/50174803/191541031-d564e8eb-60c6-4667-a960-1cff2bd910d1.png)
[ Json ]
![image](https://user-images.githubusercontent.com/50174803/191541517-0185265b-4eba-4d3a-aafe-05c509b45f6b.png)


