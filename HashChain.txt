import hashlib
seed = 'ecsc'
challenge = 'c89aa2ffb9edcc6604005196b5f0e0e4'

hash = hashlib.md5(seed.encode()).hexdigest()

print(hash)

while hash != challenge:
    hash = hashlib.md5(hash.encode()).hexdigest()
    print(hash)
