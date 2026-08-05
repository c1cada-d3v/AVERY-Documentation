# Avery's Jaw Movement, Audio, & Making an Animatronic Sing
I love animatronics because it is an interdisciplinary subject. Audio naturally comes with it. 
During Avery's prototype stage, I tested his servos with an Arduino Uno and simple servo sweep commands.

The first step I had identified in getting Avery to sing was simply getting his jaw to swing in accordance with audio/sound levels using the Arduino platform. At the time, I believe I only had a headphone audio jack connected to my computer, along with  one stereo channel led to a speaker, and the other led to my breadboard setup. I was unable to get a strong enough audio signal this way, and realized I needed an amplifier if I wanted to make this option work. 

Additionally, I considered using Mike’s Talking Skull Project (JawDuino): https://buttonbanger.com/?page_id=137

Let's talk about sound for a moment. In my original idea for Avery's jaw, I had planned on mapping audio (low to high) to servo movement (0 to 90 degrees). I was using stereo, but I was also using regular song tracks. This creates a "noise" problem, or else you have to trust that the vocals are the loudest part of your track. Avery's jaw should only be lip-syncing to the lyrics of a song as opposed to any and all input noise. If not, any background noise also triggers the servo. While I had once thought that I would just have to deal with this issue, there is a solution to this in audio editing.

With stereo, the two audio channels can be utilized to output different sound. The audio going into the ST board must be edited, and can be one of two options: audio with only lyrics (segments that only contain background music are cut from the track) or audio frequencies generated in time with lyrics playing in the other channel. Either option works, the first creates more variation because you would be able to better capture how soft or loud a singer is singing. The second is the most reliant, and you don't have to worry about the servo jaw missing a word or phrase.

I ultimately landed on the Scary Terry Audio Servo Driver boards (https://www.cowlacious.com/scary-terry-audio-servo-driver/) to tinker with for adjustability. For Avery's prototype, I only used the ST-425 to test the jaw. All manuals for the boards that actually made into the final design are in this repo, but the ST-425 is also included. I later "graduated" to the ST-450 after shorting the ST-425 on accident (it was strange, tragic, involved a very big battery, and a poorly executed last-minute Halloween idea). However, it was absolutely worth the extra money because of the on board MP3 player and additional features. The ST boards are nice because they allow you easy adjustability in terms of sensitivity to the audio input and how wide the jaw swings, with only potentiometers. The ST-450 adds buttons for moving on to different tracks along with starting and stopping, a relay, and a voltage trigger section. There is also an on-board speaker amplifier built-in.

More on the voltage trigger section: one of Avery's buttons is a poorly-disguised motion sensor. Although I don't use it regularly, it is wired and has been tested before. It was installed a little too last-minute before my presentation, and is in a hard to reach spot so it is a bit sensitive. 

The best look at how all this came together in the end is in Avery's electronic diagrams.


