- 👋 Hi, I’m @chowthecyberkorean
- 👀 I’m interested in
- def caesar_cipher(text, shift):
    result = ""
    
    # Traverse the given text
    for i in range(len(text)):
        char = text[i]
        
        # Encrypt uppercase characters
        if char.isupper():
            result += chr((ord(char) + shift - 65) % 26 + 65)
        # Encrypt lowercase characters
        elif char.islower():
            result += chr((ord(char) + shift - 97) % 26 + 97)
        else:
            result += char

    return result

# Apply Caesar cipher with a shift of 3 to "jeep"
encoded_text = caesar_cipher("jeep", 3)
encoded_text

