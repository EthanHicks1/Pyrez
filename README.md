# Pyrez: Easily way to connect to Hi-Rez API
[![Current Version](https://img.shields.io/pypi/v/pyrez.svg)](https://pypi.org/project/pyrez)
[![Documentation Status](https://readthedocs.org/projects/pyrez/badge/?version=latest)](http://pyrez.readthedocs.io/en/latest/?badge=latest)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/luissilva1044894/Pyrez/blob/master/LICENSE)
[![Runtime Version](https://img.shields.io/pypi/pyversions/pyrez.svg)](https://pypi.org/project/pyrez)
[![Contributors](https://img.shields.io/github/contributors/luissilva1044894/Pyrez.svg)](https://github.com/luissilva1044894/Pyrez/graphs/contributors)


**PyRez** is an open-source Python-based wrapper for [Hi-Rez](http://www.hirezstudios.com "Hi-Rez Studios") API that supports *[Paladins](https://www.paladins.com "Paladins Game")*, *[Realm Royale](https://github.com/apugh/realm-api-proposal/wiki "Realm Royale API Documentation")* and *[Smite](https://www.smitegame.com "Smite Game")*.

## Requirements
* [Python](http://python.org "Python.org") 3.5(or higher).
    * The following libraries are required: [`Requests`](https://pypi.org/project/requests "requests") and `requests-aeaweb`.
- [Access](https://fs12.formsite.com/HiRez/form48/secure_index.html "Form access to Hi-Rez API") to Hi-Rez Studios API.

## Installation
The easiest way to install **Pyrez** is using `pip`, Python's package manager:

```
pip install -U pyrez
```
The required dependencies will be installed automatically.
After that, you can use the library using:
```py
import pyrez
```

## Example

```py
from pyrez.api import PaladinsAPI

paladinsAPI = PaladinsAPI(devId=1004, authKey="23DF3C7E9BD14D84BF892AD206B6755C")
championsRank = paladinsAPI.getGodRanks("FeyRazzle")

if championsRank is not None:
    for championRank in championsRank:
        print(championRank.getWinratio())
```

This example will print the winrate with every [Champion](https://www.paladins.com/champions "Paladins Champions") of player **[FeyRazzle](https://twitch.tv/FeyRazzle "Sexiest Voice on Twitch")**.
