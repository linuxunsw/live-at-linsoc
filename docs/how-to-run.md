# How to Run Live@LNSC

It turns out that running presentations like this is very difficult. Here is
everything that you need to know to run your own set of student presentations.

We do our presentations in lecture rooms at UNSW, which have a specific set of
hardware. If you were to run presentations elsewhere, you'd need to get your own
hardware to replace this. Make sure you understand what your presentation room
offers. Test it ahead of time so you don't get any last-minute surprises.

## UNSW's AV Setup

* Handheld mic (good).
* Lapel mic (bad).
* Lectern mic (wrong position, a bit crunchy sometimes).
* All audio comes in through a [Dante](https://www.getdante.com/meet-dante/what-is-dante/)
  interface, via the USB dock. This appears to only give one input with the room
  mix.
* Overhead video camera. This appears as a capture card through the USB dock.
  However, its perspective (looking down on the presenter) is not ideal. Maddy
  elects not to use this camera.
* HDMI input.
* USB-C input (via dock).
* Projector(s). If multiple, you can freeze them independently to get two
  displays (eg an attendance form QR code) as well as the event banner.
* Basic room audio mixing via AV console screen.
* XLR out, can also be used for audio capture of the room mix.

## Hardware + Software Prerequisites

Slides capture:
* A dedicated AV computer.
* Capture card, capable of capturing in at least 1080p. Prioritise resolution
  over frame-rate.
* HDMI cables.

Audio capture:
* A dedicated AV computer. This can be the same one used for slides capture.
* USB for connection to UNSW AV systems.

Video capture:
* Tripod.
* Tripod to phone adapter.
* Phone.
* Repeat for more camera angles.

Resources for presenters:
* USB-C to HDMI adapter.
* Slide clicker.

## Prepping for the Event

* Book a room.
    * Give 30 mins before and after presentations for setup and teardown. Eg for
      a 2-hour presentations set, you would book for 3 hours.
    * Also add time for food if it will be provided.
* Make sure it is clear to all people involved in the running of the event who
  is responsible for what tasks. You will want people assigned to:
    * Overall management of the event, moving things along, keeping schedule.
    * Primary AV (audio-visual). In charge of mics, screen capture, projectors.
    * Video capture (one person per camera).
* Create an attendance form (or decide how tickets will be verified).

### Room inspection

* What inputs does the room's USB dock provide? Camera? Room audio via
  Dante?
* Does the AV desk have an XLR output (useful as a back-up for audio
  capture, or if the dock doesn't give room audio).
* What resolution are the projectors? Is it different via USB-C vs via HDMI?
* Places for cameras.
* Lighting controls. Decide on lighting profiles for while audience members
  are finding their seats, and for during presentations.
* While audience finds seats, we want bright room lighting.
* During presentations, we want low room lighting (probably not off, it's
  not a theater production), bright light on the presenter, low light near
  the presenter's desk (where AV).
* Do the mics work? The handheld mic is probably easiest for presenters to
  use. The lapel mics are often missing a pop filter, and may not be easy to
  attach to presenter's clothing.
* Will there be space for the AV setup and the presenter's computer?

Contact UNSW IT ahead of time if anything is broken.

* Was the room easy to find? Do we need to record a reel showing how to get
  there?

### Ahead of time info for presenters

* Make sure presenters will get there on time. Get them to arrive during the
  setup so they can get briefed.
* Make sure they bring a device to present from, or inform us that they need a
  device. Specifically, ***DO NOT*** run the capture and the presentation from
  the same device for stability reasons.
* Get presenter consent. Specifically, they should be able to consent or not
  consent to each of the following individually:
    * We will be recording their presentation.
    * We can give them a copy of their recording, or edit and upload ourselves.
    * We may include the recording on the website as an archive of the event.
    * We may use parts of the recording to promote future iterations of the
      event.
    * Make sure they understand how to withdraw their consent.
    * TODO: intellectual property and copyrights of the presentations? How can
      we balance presenters rights over their work against our desire to promote
      the event and showcase their work and the Linux Society's events.

## Promoting the Event

Our little website is in this repo. Add to it to promote the new event.

* Decide on a unified aesthetic for the website and posters.
    * Try to make the aesthetic different to previous events.
    * Create graphics and the like for use across posters, social media and
      website.
* Get info from presenters on their talks.
    * A short paragraph describing their talk in a semi-promotional way.
    * Links to socials.
    * A short description of them?
* Posters.
* Website.
    * Add a new page for this iteration of the event. Promote each speaker.
* Prepare a "between presenters" screen to use when a presenter isn't active.

## Setup

### AV

* Connect to USB-C room dock.
* Connect capture card.
* OBS:
    * Configure mic input (likely Dante). If Dante not available, connect via
      an audio interface with an XLR cable.
    * Configure capture card.
    * Ensure it records to a safe container format such that if the system
      crashes, the recording is not lost (MKV is best for this).
* ***TEST IT ALL!!!***
    * Test audio capture.
    * Test screen capture.
    * Test cameras.

### Cameras

* Tripods.
* Make sure they all aim at a consistent location. Highly recommend using a test
  subject to validate. Take note of the edges of the frame.
* Try to avoid getting the person running AV in shot.

### Presenter briefing

* Mic technique.
    * For a hand-held mic, it should be held three finger-widths from your lips.
    * When you move your head, move the mic with it.
* Where to stand.
    * Where is the centre of frame.
    * Where are the edges of the frame.
* Slide clicker (if applicable).
* Any questions?
* How will we signal them if they are short on time?

### House

* Ensure audience are comfortable.
* Consider soft gentle music (no lyrics) which can be faded out once it's time
  to begin.
* Use the "between presentations" display to show the event title. It can be run
  from the AV capture computer via the USB-C dock.
* In rooms with dual projectors, one can be frozen on this, and the other can
  show a QR code for event sign-in.

## During presentations

* Just record everything non-stop. Editors can slice and dice afterwards.
* To ensure ease of editing, avoid h265 codec (it'll need to be re-encoded to be
  used in most editors).
* Between presentations, switch back to the "between presentations display".

## After presentations

* Collect all recordings and photos.
* Edit videos together. Consider using promotional materials as a part of it,
  especially during the intro and ending.
* Some presenters may wish to upload their recordings to their own channel, or
  edit it themselves. We are happy to give them their sections of the footage.
  If they do this, we will link to their uploaded version, rather than editing
  themselves.
* If we edit it ourselves, they should be uploaded to the Linux Society YouTube
  channel.
* We should update the website to include the recordings.
* Consider creating clips to use promotionally for future events.
