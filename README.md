![CrowdStrike FalconPy](https://raw.githubusercontent.com/CrowdStrike/falconpy/main/docs/asset/cs-logo.png#gh-light-mode-only)
![CrowdStrike FalconPy](https://raw.githubusercontent.com/CrowdStrike/falconpy/main/docs/asset/cs-logo-red.png#gh-dark-mode-only)

[![CrowdStrike Subreddit](https://img.shields.io/badge/-r%2Fcrowdstrike-white?logo=reddit&labelColor=gray&link=https%3A%2F%2Freddit.com%2Fr%2Fcrowdstrike)](https://reddit.com/r/crowdstrike)<br/>

# FalconPy - The CrowdStrike Falcon SDK for Python

[![Package Status](https://img.shields.io/pypi/status/crowdstrike-falconpy?label=package%20status)](https://pypi.org/project/crowdstrike-falconpy/)
[![PyPI](https://img.shields.io/pypi/v/crowdstrike-falconpy?label=current%20version)](https://pypi.org/project/crowdstrike-falconpy/#history)
[![Release date](https://img.shields.io/github/release-date/CrowdStrike/falconpy)](https://github.com/CrowdStrike/falconpy/releases)
[![Repo status](https://img.shields.io/osslifecycle/crowdstrike/falconpy?label=repo%20status)](https://github.com/CrowdStrike/falconpy/graphs/code-frequency)
[![Commit activity](https://img.shields.io/github/commits-since/CrowdStrike/falconpy/latest)](https://github.com/CrowdStrike/falconpy/commits/main)
![GitHub forks](https://img.shields.io/github/forks/crowdstrike/falconpy?style=flat)

The FalconPy SDK contains a collection of Python classes that abstract CrowdStrike Falcon OAuth2 API interaction, removing duplicative code and allowing developers to focus on just the logic of their solution requirements.

+ [Overview](#overview-)
+ [Quick Start](#quick-start-)
+ [Documentation and Support](#documentation-and-support-)
+ [Contribute to FalconPy](#contribute-to-falconpy-)

## Overview 🔎
There are many CrowdStrike Falcon API [service collections](https://www.falconpy.io/Operations/Operations-by-Collection.html) collectively containing hundreds of [individual operations](https://www.falconpy.io/Operations/All-Operations.html), all of which are accessible to your project via FalconPy.

The CrowdStrike Falcon SDK for Python completely abstracts token management, while also supporting interaction with all CrowdStrike regions, custom connection and response timeouts, routing requests through a list of proxies, disabling SSL verification, and custom header configuration.

> If the CrowdStrike APIs were rings of great power, that the Dark Lord Sauron gifted to the kings of dwarves, elves and men, then CrowdStrike's FalconPy would be the One Ring.
> 
> _"One SDK to rule them all, One SDK to find them, One SDK to bring them all and in the darkness bind them."_

[![Downloads](https://static.pepy.tech/personalized-badge/crowdstrike-falconpy?left_text=package%20installs/month&left_color=grey&right_color=blue&period=month)](https://pepy.tech/project/crowdstrike-falconpy)
[![Development Installs](https://static.pepy.tech/personalized-badge/crowdstrike-falconpy-dev?left_text=development%20package%20installs/month&left_color=grey&right_color=blue&period=month)](https://pepy.tech/project/crowdstrike-falconpy-dev)

#### Supported versions of Python
The CrowdStrike Falcon SDK for Python was developed for Python 3. Current versions of FalconPy provide support for Python versions `3.7` - `3.13`. Every commit to the FalconPy code base is unit tested for functionality using all versions of Python the library currently supports.

> [!NOTE]
> Developers working with Python version `3.6` will need to leverage versions of FalconPy less than `1.4.0`.

[![PyPI - Implementation](https://img.shields.io/pypi/implementation/crowdstrike-falconpy)](https://pypi.org/project/crowdstrike-falconpy/#files)
[![PyPI - Wheel](https://img.shields.io/pypi/wheel/crowdstrike-falconpy)](https://pypi.org/project/crowdstrike-falconpy/#files)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/crowdstrike-falconpy?label=supported%20versions)](https://github.com/CrowdStrike/falconpy/actions/workflows/unit_testing_ubuntu.yml)

#### Supported Operating Systems
The FalconPy SDK is unit tested on the following operating systems.

[![macOS](https://img.shields.io/badge/-macOS-silver?logo=apple&style=for-the-badge&labelColor=gray)](https://www.apple.com/macos/)
[![Ubuntu](https://img.shields.io/badge/-Ubuntu-964?logo=ubuntu&style=for-the-badge&labelColor=tan)](https://ubuntu.com/)
[![Windows](https://img.shields.io/badge/-Windows-blue?logo=windows&style=for-the-badge&labelColor=darkblue)](https://www.microsoft.com/en-us/windows/)

FalconPy will also run on any of the following operating systems.

[![Amazon Linux](https://img.shields.io/badge/-Amazon-darkgreen?logo=amazon&style=for-the-badge&labelColor=teal)](https://aws.amazon.com/amazon-linux-ami/)
[![CentOS](https://img.shields.io/badge/-CentOS-magenta?logo=centos&style=for-the-badge&labelColor=purple)](https://www.centos.org/)
[![Fedora](https://img.shields.io/badge/-Fedora-teal?logo=fedora&style=for-the-badge&labelColor=darkblue)](https://getfedora.org/)
[![RedHat](https://img.shields.io/badge/-RedHat-red?logo=redhat&style=for-the-badge&labelColor=maroon)](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux)
[![Arch](https://img.shields.io/badge/-Arch-darkgray?logo=archlinux&style=for-the-badge&labelColor=gray)](https://archlinux.org/)

[![Debian](https://img.shields.io/badge/-Debian-darkred?logo=debian&style=for-the-badge&labelColor=red)](https://www.debian.org/)
[![Kali](https://img.shields.io/badge/-Kali-gray?logo=kalilinux&logoColor=red&style=for-the-badge&labelColor=black)](https://www.kali.org/)
[![Pop! OS](https://img.shields.io/badge/-Pop!%20OS-orange?logo=popos&logoColor=black&style=for-the-badge&labelColor=yellow)](https://pop.system76.com/)
[![SUSE](https://img.shields.io/badge/-SUSE-yellow?logo=suse&style=for-the-badge&labelColor=orange)](https://www.suse.com/)
[![openSUSE](https://img.shields.io/badge/-openSUSE-orange?logo=opensuse&style=for-the-badge&labelColor=darkorange)](https://www.opensuse.org/)

Details regarding supported operating systems and Python versions, and project security and testing procedures can be found [here](https://github.com/CrowdStrike/falconpy/blob/main/SECURITY.md).

### Components
The FalconPy SDK provides two distinct methods for interacting with CrowdStrike's API. 

| **[Service Classes](#service-classes)** | **[The Uber Class](#the-uber-class)** |
| :-- | :-- |
| <BR/>[![Service Classes](https://raw.githubusercontent.com/CrowdStrike/falconpy/main/docs/asset/service-class-relationships.png)](#service-classes) | [![The Uber Class](https://raw.githubusercontent.com/CrowdStrike/falconpy/main/docs/asset/uber-class-relationships.png)](#the-uber-class) | 
| Each Service Class represents a single CrowdStrike API service collection providing an interface to the [operations available](https://www.falconpy.io/Operations/Operations-by-Collection.html) within that service collection.| An all-in-one class that provides a singular interface for [all operations](https://www.falconpy.io/Operations/All-Operations.html) in every CrowdStrike API service collection. |


### Service Classes
Representing a single CrowdStrike Falcon API service collection, each Service Class has a method defined for [every operation available](https://www.falconpy.io/Operations/Operations-by-Collection.html) within that service collection.

#### Available Service Classes
For each CrowdStrike Falcon API service collection, a matching Service Class is available in the FalconPy library. For a complete list of service collections and their related Service Class, please review the [Operations by Collection](https://www.falconpy.io/Operations/Operations-by-Collection.html) page on [falconpy.io](https://falconpy.io).
