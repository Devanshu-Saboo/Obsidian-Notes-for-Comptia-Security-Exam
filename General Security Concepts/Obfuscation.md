Obfuscation is simply the process of taking something that would normally be very easy to understand and making it very hard to understand. It is important to know that obfuscation is *not* the same as encryption. If you know how the obfuscation was done, you can reverse it and get the original data back, so we are effectively hiding information in plain sight. There are 3 types I need to know:
1. ==🟠Steganography==
2. ==🟠Tokenization==
3. ==🟠Data masking==

### Steganography
This comes from the Greek for "concealed writing". It means hiding a message inside something else, so that nobody even realizes there is a message to look for. The file that holds the hidden data is called the ==🟠covertext==. ==🟢ex. Hiding a secret message inside an image, where the picture looks completely normal to everyone but the person who knows how to extract the data==

It is often called ==🟠security through obscurity==. That means if somebody finds out how the data was hidden then it is very easy for them to recover it, so by itself this is not real security. Some other ways it can be done are:
1. ==🟠Image==: Embed the message within the pixels of the image
2. ==🟠Audio and Video==: The same idea but in a sound file or a video. A video is basically a lot of images, so it can hide a much larger amount of data.
3. ==🟠Network based==: Embed the message in the packets, such as in TCP packets
4. ==🟠Invisible watermarks==: ==🟢ex. The tiny yellow dots that some printers add to every page they print==

### Tokenization
Tokenization is replacing the sensitive data with a non-sensitive placeholder called a token. The original data and the token have no mathematical relationship, which means this is not encryption or hashing, and the token cannot be reversed to get the original back. ==🟢ex. An SSN of 266-12-1112 is replaced by a completely different looking number==

A common everyday example is paying with your phone:
1. When you first add your credit card to the phone, it contacts a token service server
2. When you pay, your phone sends a temporary token instead of your real card number
3. The token is used once and then thrown away, so if somebody captures it, it is useless to them

### Data Masking
Data masking is hiding only a part of the original data. ==🟢ex. A receipt showing **** **** **** 1234, where only the last four digits of the card number are visible==

The full number is still known by the card company, we are only hiding it from the person looking at the screen or the receipt. A customer service representative might also see only part of your details, depending on their permissions. The data might still be fully intact in storage, it is just hidden from view. This protects PII (Personally Identifiable Information) and other sensitive data. Some different ways to mask the data are substituting, shuffling, encrypting and masking out.

# Previous Topic
[[Encryption Technologies]]
# Previous Section
[[Encrypting Data]]
# Next Topic
[[Hashing and Digital Signatures]]
