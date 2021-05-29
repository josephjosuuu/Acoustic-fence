# Acoustic-fence

Based on [Impulse CET](https://pages.github.com/) Hackathon.

**Problem Statement:** (Scenario 1) There has been a constant rise in the number of attacks by wild animals on lands near forest or such other areas. Primarily agricultural land, which happens to be free food for the invaders.

**Task:** Propose a solution to improve the situation for those affected by such attacks.

##### Team:
1. Aswin A (aswinajith6082@gmail.com) [@aswinajith6082]
2. Christy John Manoj (christyjohnmanoj@gmail.com) [@chrisssssss323]
3. Joseph John (josephjosuuu10@gmail.com) [@Appachan10]

### Wild animal attacks and existing measures

- As many as 153 farmers, including 93 tribal farmers, have cultivated paddy on 200 acres of the 250 acres of land under the **Chekadi Padashekharam, Wayanad**. Nearly 30 acres of paddy crops have been destroyed by wild animals in the last year.
- Over Rs 5 crore losses were caused within the last 18 months due to wild elephants roaming around **Aralam farm in Kannur district**, located near the Aralam wildlife sanctuary.
- Over 100 hectares of farmlands in **Tholambra, Thrikkadarippoyil, Palottuvayal, Palachippara, Sivapuram, Padupara, Alachi, Thillankeri, and Mudakkozhi areas in Puralimala valley, Kannur** is under threat of monkeys and wild boars.

##### Current prevention methods used by farmers in Kerala:

- Installing electric fences running to several kilometers on the forest borders (But the animals enter human habitats and farms after destroying them).
- Using explosives (which can cause severe injuries to wild animals leading to certain death).
- Poisoning and hunting wild animals (Which causes wildlife extinction and environmental imbalance).

# Solution: Acoustic-fence

### Block diagram

![Untitled](https://user-images.githubusercontent.com/49588749/120074395-4d675600-c0ba-11eb-8b7d-155ad335dd15.png)




### Solar Power Source:

- The Raspberry pi board is powered by solar power.
- Most economical and renewable source of energy.
- Energy stored during day-time is used for the 24 hour real-time operation.
- Solar cells extra energy stored can be used to power up LED's setup in the farm.


### Voice Recognition Module :

![2](https://user-images.githubusercontent.com/62739750/120079935-00907900-c0d4-11eb-8db2-44849950018c.jpeg)

- Raspberry pi with RS232 converter gives in the real time observed input.
- Analog input from mic is coverted into digital signal by the RS232 module.
- Raspberry pi module processes the audio input for detection and segregation.

### Sound selection :

- Animal predicted by the trained model

### Speaker :

![3](https://user-images.githubusercontent.com/62739750/120079943-0ede9500-c0d4-11eb-8149-e290fe232f53.jpg)

- The speaker gives out infrasonic sound and ultrasonic sounds according to the animal predicted.
- The sound is kept out of human hearing range.
- 14-16hz voice clip for elephants.
- Ultrasonic voice clips for Boar and monkey.

### Send Message :

![4](https://user-images.githubusercontent.com/62739750/120079955-19009380-c0d4-11eb-92bb-9967a52d4551.jpeg)

- SIM900A GSM module is used to transmit message to farmer.
- Uses HTTP and MQTT over the Local Area Network used to transmit message.
- Emergency messages of intruder entry into field is passed onto the farmer, to take physical action(if needed).
