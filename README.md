def caesar_decrypt(cipher_text, shift):
result = '' 
for char in cipher_text:
if char.isalpha():
base = ord('A') if char.isupper() 
else ord('a')
result += chr((ord(char) - base - shift) % 26 + base) 
else:
result += char
return result 
def main():
print("=== أداة فك تشفير Caesar بدون مفتاح ===")
cipher_text = input("أدخل النص المشفر: ")
print("\nالمحاولات الممكنة لفك التشفير:\n")
for shift in range(1, 26):
decrypted =
caesar_decrypt(cipher_text, shift)
print(f"[مفتاح {shift}] {decrypted}")
if name == "main":
main()
