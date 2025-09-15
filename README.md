# BTVN-4.1
def btvn4_1(text, k):
    result = ""
    k = k % 26
    for char in text:
        if char.isalpha():
            base = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - base + k) % 26 + base)
        else:
            result += char
    return result
k = 48  
plaintext = "Tran Thi Cam Tien"  
ciphertext = btvn4_1(plaintext, k)
print("Plaintext :", plaintext)
print("Ciphertext:", ciphertext)
