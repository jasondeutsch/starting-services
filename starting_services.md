# Starting Services

This repository contains practices that I consider best when designing and maintaining software. The following information is presented as personal opinion, rather then concrete best practice. While much of what is described is generalizable to various technologies the content will be oriented around microservices, the Go language, and cloud native environments.

## Documentation

### README.md

README needs no introduction. It is the first place contributors will look to become oriented with the project and there is nothing that forshadows frustration more than an absent or lacking README.

READMEs by thier nature are specific to the repository they describe, however the following are good default starting sections:

#### 1 Build and Run

The shortest path to getting the program up and running is often the best path. 
* Utilize Makefiles to provide shortcuts and documentation
** [Taskfile](https://taskfile.dev/) is an alternative to Makefile
* Documentation MUST reference Makefile tasks where appropriate 
  
ex.
```Make
GO_VERSION := 1.22

.PHONY: install-go init-go

setup: install-go init-go


install-go:
  wget "https://golang.org/dl/go$(GO_VERSION).linux-amd64.tar.gz"
  sudo tar -C /usr/local -xzf go$(GO_VERSION).linux-amd64.tar.gz
  go$(GO_VERSION).linux-amd64.tar.gz

init-go:
  echo 'export PATH=$$PATH:/usr/local/go/bin' >> $${HOME}/.bashrc
  echo 'export PATH=$$PATH$${HOME}/go/bin' >> $${HOME}/.bashrc


```

#### 2 Configurations and Environments
#### 3 Dependencies
#### 4 Troubleshooting
#### 5 Common Use Cases
#### 6 Software Milestones


