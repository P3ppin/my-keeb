**Planning**
Today I started researching different keyboard layouts (like the 60%, 96%, and all in between).
I want to make a 100% or 1800 keyboard. I think the 1800 is perfect, because i don't really need the extra 8 keys, but a numpad is fine. Imma make a 1800 keyboard, so with 96 keys.

**Designing the PCB**
<img width="1287" height="379" alt="image" src="https://github.com/user-attachments/assets/b085e6a4-f837-4e37-a53a-9d455a6f5426" />
I started laying out the keys, where I wanted them to be. I used some reference keyboards to do this, so I was sure I didn't miss any important keys.


<img width="1508" height="415" alt="image" src="https://github.com/user-attachments/assets/7960cb06-ff00-4a30-b6d0-933c228d9451" />
I compressed the matrix a little, so  I spared 1 column. With all the keys it would fit (19 x 6 matrix), so 25 pins, but then I only had 1 pin left. I also want to include a rotary encoder, but I need atleast 2 pins for that, maybe even 3 for the clicking function.

My plan for now is to compress all the keys into a 11 x 10 matrix, so I have 6 pins left. I now made the schematic look like the key layout, but that doesnt really matter, so I will just make a rectangle. I'm also curious how the programming will work, do I have to bind every key individually, or how does that work? But that's a question for later.

I also checked if the switch counting was correct, by duplicating a key, and the number the switch got was 105 instead of 108, that ment that I had deleted the 105 key, so that there weren't 107 keys, but 106 keys.

Now I can delete all the keys and make a matrix from 11 x 10, with 106 keys.


Now I've added the keys, I selected everything, and looked at the selected count to make sure I had placed the correct ammount of keys. It was 212 items, divided by 2 = 106, so it was right and I could move on to wiring.


<img width="948" height="822" alt="image" src="https://github.com/user-attachments/assets/d2d80195-994a-4219-81e7-35be3b3d0f49" />



I now added the rotary encoder, I don't know if the one included in the grant is with or without the switch, but I added it just in case
<img width="1250" height="825" alt="image" src="https://github.com/user-attachments/assets/538465b8-9a6b-4166-958d-9fdd43455290" />


I rechecked everything with the amount of keys, and it turns out, I actually need 110 keys for my layout, I had duplicate labels. This shows how important double (double) checking is!

Now I'm all set with the schematic, I can move on to designing the layout/rest of the PCB.


When I imported all the footprints in the PCB-editor, I got the warnings: _Warning: No net found for component SW23 pad MP (no pin MP in symbol). Warning: No net found for component SW23 pad MP (no pin MP in symbol)._

I solved this by editing the symbol and adding two MP pins and grounding them (for extra safety):
<img width="390" height="292" alt="image" src="https://github.com/user-attachments/assets/92896ff6-817b-4366-aae9-7256ec4f46da" />
