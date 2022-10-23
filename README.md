# Touchdesigner - Audio to Eos


<img width="626" alt="Screen Shot 2022-10-23 at 12 40 19 PM" src="https://user-images.githubusercontent.com/70780576/197414451-62f2f877-04b7-4c1a-9267-0c522d8f159d.png">

[Download File](https://github.com/jshea2/Touchdesigner-Audio-to-Eos/releases/tag/v1.0])

This Touchdesigner file processes incoming audio signal to trigger Eos channels in two seperate ways
  - **Thresh** - Trigger two lighting channels by threshold. So when the audio is below a the threshold it's on first lighting channel, then when audio goes above the threshold it triggers the second one.
  - **Intens** - This takes the audio signal and converts the amplitude to a 0-100 intensity value for the desired lighting channel.

## Setup

- **Patch Audio**
    - In Touchdesigner by default the audio device is set to your computer's default audio device configuration. If you want to change this you can zoom into the UI operator and you'll see two nodes on the left "audiodevin1" and "audiodevin2". If you click on it and the properties don't show up, click "P", then adjust the "driver".
- **Send commands to Eos**
    - In Touchdesigner set the IP, Port In and Out to match Eos console. Find Eos IP by pressing "About" key (see below for ports).
- **Send Cue Triggers to Touchdesigner**
    - In Eos (Setup > System Settings > Show Control > OSC) Set the "OSC UDP TX IP ADDRESS" to the Touchdesigner computer's IP.
    - Set "OSC CUE SEND STRING" to match Touchdesigner's "Eos Cue Send String". 
        - Example: `/touch/`
    - Pre and Post Cues are to turn the audio device off so you only have it trigger in the Active Cue, then until either the Post Cue is triggered. Pre isn't needed for the running of the show, but is helpful during Tech, so you don't have to manually turn it back off to re-trigger it
    - If Eos "Goes to Cue Out" or "Cue 0". The audio device will also turn off.

## Example

https://user-images.githubusercontent.com/70780576/197409774-05350d87-09be-4259-b283-238d4f1bca4f.MOV

The video example shows the 'trigger by threshold'. An actor was speaking offstage into a microphone, then this was sent to the audio mixer and Touchdesigner. Lighting was used with neon led tape to shape a mouth. one lighting channel for closed shape and one lighting channel for open shape. This gives the effect of the mouth opening and closing dynamically when someone is talking in real-time.
