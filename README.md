# Touchdesigner - Audio to Eos

This Touchdesigner file processes incoming audio signal to trigger Eos channels in two seperate ways
  - 1. Trigger 2 lighting channels by threshold. So when the audio is below a the threshold it's on first lighting channel, then when audio goes above the threshold it triggers the second one.
  - 2. This takes the audio signal and converts the amplitude to a 0-100 value for the desired lighting channel.

## Example

https://user-images.githubusercontent.com/70780576/197409774-05350d87-09be-4259-b283-238d4f1bca4f.MOV

The video example shows the 'trigger by threshold'. An actor was speaking offstage into a microphone, then this was sent to the audio mixer and Touchdesigner. Lighting was used with neon led tape to shape a mouth. one lighting channel for closed shape and one lighting channel for open shape. This gives the effect of the mouth opening and closing dynamically when someone is talking in real-time.
