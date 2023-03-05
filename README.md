# Free ENS - Open-source ENS top-level domain aggregator for free subdomain registration.
# https://rfedoskin.github.io/Freeens-dapp-front/

How does Dapp work and how do you add your ENS top-level domain for subdomain registration (paid or free, it's up to you)?

1. How it works
2. How to add your ENS top-level domain for subdomain registration (ENS Smart-contracts)
3. How to add your ENS top-level domain in Dapp

# 1. How it works?

- You delegate your top-level domain to ENS smart-contract to enable subdomains registration.
- Set the price for registration and referral percentage.
In the repository https://github.com/rfedoskin/Freeens-dapp-front in the config.json file, write down the parameters of your domain and make a commit, if everything is fine, then I approve the commit and your domain will appear in the list at https://rfedoskin.github.io/Freeens-dapp-front/ and you can give this link to your audience for registration. 
- Any user can register a subdomain for himself. He doesn't need your permission or trust. Everything works on the terms of the ENS smart-contract to which you have permanently delegated your domain.
- No one except the owner of the subdomain has the right to change or delete something. The former owner who delegated his top-level domain can only manage the price for registering subdomains, stop registering new ones, transfer configuration rights and change the referral percentage.
- If the domain that was delegated to the ENS contract has expired, then all registered subdomains are reset and the domain is again available for open registration. But anyone can extend it so that such a case does not happen.
- Subdomain users can use all the same features as top level name users.

# 2. How to add your ENS top-level domain for subdomain registration (ENS Smart-contracts)?

# Attention
# If your follow all the steps in this manual, you will no longer be the owner of this domain, you can only stop registering subdomains, and change the prices for  registration in ENS smart-contract.

2.1 Go to https://etherscan.io/enslookup for copy TokenID.

Enter your domain name:

![image 1-2](https://user-images.githubusercontent.com/55558577/222940334-0cffeb04-137b-469a-bce1-c687a1791ae4.png)

2.2 Go to ENS Smart-contract and call “approve” method.
https://etherscan.io/token/0x57f1887a8bf19b14fc0df6fd9b2acc9af147ea85#writeContract

<img width="1067" alt="image" src="https://user-images.githubusercontent.com/55558577/222940386-42a39361-89e5-43d1-872a-9ca123bcd418.png">

2.3 Go to ENS: Subdomain Registrar smart-contract and call “configureDomain ” method.
https://etherscan.io/address/0xe65d8aaf34cb91087d1598e0a15b582f57f217d9#writeContract

<img width="1204" alt="image" src="https://user-images.githubusercontent.com/55558577/222940998-3076b8ad-7b42-4917-80b3-cfc3474c1d5a.png">

# 3. How to add your ENS top-level domain in Dapp

In the repository https://github.com/rfedoskin/Freeens-dapp-front in the config.json file, write down the parameters of your domain.

<img width="1073" alt="image" src="https://user-images.githubusercontent.com/55558577/222940520-f66730a2-8ed0-49a0-ac94-81bd37e1af00.png">

id - ordinal number of the list, enter the last one +1.

name - name of your top-level domain without .eth.

section:
“paid” - if your domain is paid for subdomain registration,
“free” - if your domain is free for subdomain registration.

paid:
“false” - if domain is free for subdomain registration,
“true” - if your domain is paid for subdomain registration.

price - value in ETH. If the domain is free, then "0".

referrer - referrer for this domain. If set to null, the default referrer will be used.

resolver - resolver for this domain. If set to null, then the default resolver will be used.

pageBanner and modalBanner - These are banner ads that the user needs to see if the user wants to register this domain for free. This is discussed individually, so by default put everywhere - "null"


After making changes to the config.json file, you can make a commit, and write to me in telegram https://t.me/romanfedoskin so that I accept this commit, or if something is not correct, I could contact you.

You can also fork and raise your dapp with your conditions and domain list.
