# Docker
## Unix
### Remove all images 
`docker rmi -f $(docker images -aq)`
### Remove all containers 
`docker rm -vf $(docker ps -aq)`
## Windows
### Remove all images 
`docker images -a -q | % { docker image rm $_ -f }`
### Remove all containers
`docker container ls -a -q | % { docker rm $_ -f }`

# GitHUB
## Login to private repo from server
`export CR_PAT=your_access_token`

`echo $CR_PAT | docker login ghcr.io -u GH_USERNAME --password-stdin`

## How to create private token to access private image from the server
`https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry`
