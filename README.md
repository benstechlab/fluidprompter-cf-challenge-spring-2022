# FluidPrompter submission for CloudFlare Developers Challenge Spring 2022

This repo contains FluidPrompter submission materials for CloudFlare Developers Challenge Spring 2022.

I intend to make FluidPrompter a commercial app and so will not open source the entirety of its code base, but rather just share the CloudFlare bits and pieces the community may find interesting!

## Live Demo of FluidPrompter

1. Visit https://app.fluidprompter.com/
2. The websocket connection is currently "opt-in", you have to click the little cloud icon at the top right, and choose "Enable Cloud Remote" from the drop down menu.
3. The websocket connection will connect within a second or two.
4. You may now click the QR Code button also in the top right toolbar next to the cloud icon to open a remote control on your phone. Scan the QR Code that appears to open the remote on your phone.
5. The remote control will also connect a websocket connection within a second or two and you will be able to issue 5 commands to the teleprompter app:
  - Play/Pause
  - Page Up/Page Down
  - Speed Up/Speed Down

## Interesting Aspects for CloudFlare Community

This project is fundamentally very similar in nature to the web chat sample application published by cloudflare. However there are a few things I didn't like about the CloudFlare sample app:

1. The CloudFlare Sample App was/is ugly (for the sake of simplicity/purity I'm sure :-) ). I'm using React with Material UI v5 in this app and wrote a react hook component that maintains the websocket connection for either of my React Pages. To keep things loosely coupled I also use a React Message Bus library called `react-bus`.
2. The CloudFlare Sample App was written as one massive `.mjs` file which is hard to follow and IMHO not maintainable. I wrote my cloudflare worker using typescript with the recently updated wrangler v2. I've found a lack of good typescript samples for CloudFlare workers.

## Willing to Share More

The live demo is functional on the day of submission, however, I will copy over a subset of code (the interesting cloudflare bits) into this repo for public consumption without open sourcing my entire react app.

I am at the Mongo World Conference as of the deadline, already out of sync from timezone travels and may sneak in another commit after the submission deadline only to perform the above distilling of the core cloudflare pieces into this public repo. The demo app is fully functional now!


## Where did this idea come from?

During Covid while working from home, I started a YouTube channel from my home office. Sometime I re-recorded the same bit of talking quite a few times if I didn't get it right. I thought a teleprompter could help keep me on track with my line of thought, reduce re-takes and increase the efficiency of video editing later!

I found many of the available teleprompter apps were missing key features or were very platform specific (only worked on windows desktop or mac desktop or iPad - rarely or never more than one platform). So I decided to try my hand at writing my own!
