.DEFAULT_GOAL := all
MAKEFLAGS += --warn-undefined-variables --no-print-directory
SHELL := /bin/bash

IMAGE := healthchecks
PLATFORMS ?= amd64
VERSION := $(shell curl -s -u ":$(GITHUB_TOKEN)" -L -- https://api.github.com/repos/healthchecks/healthchecks/releases/latest | jq -r '.tag_name' | grep -Eo '([0-9]+\.){2}[0-9]+')

include ../buildx/Makefile
