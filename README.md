import requests
import random
from colorama import *
g = Fore.GREEN
r = Fore.RED
y = Fore.YELLOW
c = Fore.CYAN
print(c + requests.get('http://artii.herokuapp.com/make?text= R  O  U  X  ').text)
print('        𝑫𝑬𝑽  : @youssef :: @youssef')
print('\033[0;37m')
id = input("  [+] Enter Id : ")

token = input("  [+] Enter Bot Token : ")

litters = 'qwertyuiopasdfghjklzxcvbnm1234567890'
u = '.'

print('')
hea = {
        'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9',
        'accept-encoding': 'gzip, deflate, br',
        'accept-language': 'en-US,en;q=0.9,ar;q=0.8',
        'cache-control': 'max-age=0',
        'sec-ch-ua': '" Not;A Brand";v="99", "Google Chrome";v="91", "Chromium";v="91"',
        'sec-ch-ua-mobile': '?0',
        'sec-fetch-dest': 'document',
        'sec-fetch-mode': 'navigate',
        'sec-fetch-site': 'same-origin',
        'sec-fetch-user': '?1',
        'upgrade-insecure-requests': '1',
        'user-agent': 'Mozilla/5.0(Windows NT 10.0;Win64;x64) AppleWebKit/537.36(KHTML, like Gecko) Chrome/91.0.4472.124 Safari/537.36'
    }
while True:
    user = str("".join(random.choice(litters)for x in range(1)))
    user1 = str("".join(random.choice(litters)for x in range(2)))
    uer = str("".join(random.choice(litters)for x in range(1)))
    uer1 = str("".join(random.choice(litters)for x in range(2)))
    use = str("".join(random.choice(litters)for x in range(1)))
    use1 = str("".join(random.choice(litters)for x in range(2)))
    usernames = user + u + user1
    use = u + use1 + use
    uer = uer1 + u + uer 
    tiko = f'https://www.tiktok.com/@{usernames}?'
    to = f'https://www.tiktok.com/@{use}?'
    tio = f'https://www.tiktok.com/@{uer}?'
    reqsnd = requests.get(tiko, headers=hea).status_code
    if reqsnd == 404:
            print(g + f' [+] {usernames} ✅ ')
            bot = f"https://api.telegram.org/bot{token}/sendMessage?chat_id={id}&text=𝙐𝙎𝙀𝙍 : {usernames}\n𝘽𝙔 : @youssef"
            requests.get(bot)
    else:
         print(r + f' [+] {usernames} ❌ ')
    reqsnd = requests.get(to, headers=hea).status_code
    if reqsnd == 404:
            print(g + f' [+] {use} ✅ ')
            bot = f"https://api.telegram.org/bot{token}/sendMessage?chat_id={id}&text=𝙐𝙎𝙀𝙍 : {use}\n𝘽𝙔 : @youssef"
            requests.get(bot)
    else:
         print(r + f' [+] {use} ❌ ')
    reqsnd = requests.get(tio, headers=hea).status_code
    if reqsnd == 404:
            print(g + f' [+] {uer} ✅ ')
            bot = f"https://api.telegram.org/bot{token}/sendMessage?chat_id={id}&text=𝙐𝙎𝙀𝙍 : {uer}\n𝘽𝙔 : @youssef"
            requests.get(bot)
    else:
         print(r + f' [+] {uer} ❌ ')

#==========================================================================
