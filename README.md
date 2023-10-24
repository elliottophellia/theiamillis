<p align='center'>
<img src='https://i.ibb.co/QJ78JGn/kaga.png' width='300'/><br/><img src="https://img.shields.io/badge/KAGA%20REVERSE%20IP%20LOOKUP-pink?style=for-the-badge"/><br/>
Kaga is a reverse IP lookup tool written in Python, comes with a GUI and API to make it easy to use in any environment. The name Kaga itself is taken from virtual youtuber <a href="https://virtualyoutuber.fandom.com/wiki/Kaga_Nazuna">Kaga Nazuna</a> and <a href="https://virtualyoutuber.fandom.com/wiki/Kaga_Sumire">Kaga Sumire</a> from <a href="https://vspo.jp/">VSPO</a>.<br/><br/><img src="https://img.shields.io/badge/PYTHON-3.10-pink?style=flat-square"/> <img src="https://img.shields.io/badge/LICENE-GPL2.0-pink?style=flat-square"/> <img src="https://img.shields.io/badge/VERSION-1.0.3-pink?style=flat-square"/><br/><a href="https://www.paypal.com/paypalme/elliottophellia"><img src="https://img.shields.io/badge/BUY%20ME%20A%20COFFEE-pink?style=for-the-badge&logo=paypal&logoColor=black"/></a> <a href="https://saweria.co/elliottophellia"><img src="https://img.shields.io/badge/TRAKTIR%20SAYA%20KOPI-pink?style=for-the-badge&logo=BuyMeACoffee&logoColor=black"/></a>
</p>
<h1></h1>
<p align='center'>
<a href="#Changelogs"><img src="https://img.shields.io/badge/CHANGELOGS-pink?style=for-the-badge"/></a> <a href="#Prerequisites"><img src="https://img.shields.io/badge/PREREQUISITES-pink?style=for-the-badge"/></a> <a href="#Usage"><img src="https://img.shields.io/badge/USAGE-pink?style=for-the-badge"/></a> <a href="#Host"><img src="https://img.shields.io/badge/HOST-pink?style=for-the-badge"/></a> <a href="#Screenshot"><img src="https://img.shields.io/badge/SCREENSHOT-pink?style=for-the-badge"/></a> <a href="#Licence"><img src="https://img.shields.io/badge/LICENCE-pink?style=for-the-badge"/></a> <a href="#Disclaimer"><img src="https://img.shields.io/badge/DISCLAIMER-pink?style=for-the-badge"/></a>
</p>
<h1></h1>

# Changelogs - v1.0.3

###  Back-end :
- Dropping `httpx` in favor of `requests-html` for better scraping capability
- Dropping `beautifulsoup4` because `beautifulsoup4` already integrated in `requests-html`
- Make domain/ip validation to check if domain/ip is valid or not

###  Docs :
- Add API Documentation

# Prerequisites

- python - ^3.10
- fastapi - ^0.103.2
- requests-html - ^0.10.0
- validators - ^0.22.0

# Usage

## GUI

Simply download the newest version from [Releases](https://github.com/elliottophellia/kaga/releases) and run it or visit our demo at [kaga.rei.my.id](https://kaga.rei.my.id)

(Keep in note that our demo have limitation of 30 requests in 10 seconds)

## API

### Endpoint
```
/api/reverseip
```

This endpoint can be accessed with POST, PUT methods with payload data `domain` or GET method with parameter `domain`.

#### POST, PUT

Payload:
```
{
    "domain": "example.com"
}
```
Example:
```
curl -s -X POST -d "domain=example.com" http://127.0.0.1:3000/api/reverseip | jq .ReqResult.ResultList
```

#### GET

Parameters:
```
/api/reverseip?domain=example.com
```
Example:
```
curl -s http://127.0.0.1:3000/api/reverseip?domain=example.com | jq .ReqResult.ResultList
```
# Host

### 1. Clone this repository
```
git clone http://github.com/elliottophellia/kaga
```
### 2. Change directory to kaga
```
cd kaga
```
### 3. Install dependencies
```
pip install -r requirements.txt
```
### 4. Run kaga
```
uvicorn main:app --host 0.0.0.0 --port 3000
```

# Screenshot

![1](https://i.ibb.co/FXGCKbM/Capture.png)
![2](https://i.ibb.co/zNTS35N/Capture1.png)

# Licence

This project is licensed under the GPL 2.0 License - see the [LICENCE](https://github.com/elliottophellia/kaga/blob/main/LICENSE) file for details

# Disclaimer

This project is for educational purposes only any kinds of actions and or activities related to the material contained within this project is solely your responsibility The misuse of the information in this project can result in criminal charges brought against the persons in question The author will not be held responsible in the event any criminal charges be brought against any individuals misusing the information in this project to break the law.