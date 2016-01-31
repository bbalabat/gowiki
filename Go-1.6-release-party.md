### What's happening?
To celebrate the release of Go 1.6 we're organising a world wide release party on February the 17th, 2016. 

#### Hang on, did you say Go 1.6 ships on the 17th of February?
Nope! Go 1.6 ships when it's ready. With that said, things are looking pretty good for a mid Feb release. Using the power of software estimation, a date was plucked from the aether that happened to coincide with several meetups that were already in the works.

### Sounds awesome, how can you get involved?
- If you host a Go user group or meetup, schedule a meetup on the 17th of Feb and celebrate with Gophers around the world.
- If you're a member of a Go user group or meetup, pester your organiser and let them know you'd like to participate.

After the event post a photo, make a video, write a blog post, scribble on your Facebook wall, or tweet something pithy. Let's see how big we can make the celebration.

Don't forget to add your details :point_down: right here.

#### Who's involved?
Here is a list of the groups who are participating.
- [Sydney Go users' group](http://www.meetup.com/golang-syd/events/228276309/)
- [Go-Miami](http://www.meetup.com/Go-Miami/events/228280324/)
- [San Diego Gophers](http://www.meetup.com/sdgophers/events/228129827/)
- [PDX Go](http://www.meetup.com/PDX-Go/events/228220792/)
- [GopherConIndia](http://www.gophercon.in/)
- [Ukrainian Golang User Groups](http://www.meetup.com/uagolang/events/228343484/)
- [Lviv Golang Group](http://www.meetup.com/Lviv-Golang-Group/events/228344940/)
- [Edmonton Go](https://edmontongo.org/) (Feb 22)
- [Software Craftsmanship Toulouse](http://www.meetup.com/fr-FR/Software-Craftsmanship-Toulouse/events/228285655/)
- [Polish GLUG Meetup](http://www.meetup.com/GoLang-User-Group-Wroclaw/events/228369658/)
- [Google Developer Group Gigcity](http://www.meetup.com/GDG-Gigcity/events/228373161/)
- [Golang Montréal](https://golangmontreal.org) (Feb 22nd)
- [Golang Vietnam](https://www.facebook.com/events/1651152271814093/) (Feb 23)
- [Gophers Katowice](http://www.meetup.com/Gophers-Katowice/events/228375778/)
- [GoSF](http://www.meetup.com/golangsf/events/226090306/)
- [Boston Golang](http://www.meetup.com/Boston-Go-lang-User-Group/events/228398963/)
- [Go-Tampa](http://www.meetup.com/Go-Tampa/events/227365472/)
- [Atlanta](http://www.meetup.com/Go-Users-Group-Atlanta/events/228336134/)
- [GoAKL](http://www.meetup.com/Go-AKL/events/228436705/)
- [Golang Barcelona](http://www.meetup.com/es-ES/Golang-Barcelona/events/228438675/)
- [Golang Singapore](http://www.meetup.com/golangsg/events/228148961/)
- [Go Maryland](http://www.meetup.com/Go-Maryland/events/228445301/) (February 18)
- [Orange County Gophers](http://www.meetup.com/Orange-County-Gophers/events/228458630/)
- [Central Jersey Tech Meetup](http://www.meetup.com/Central-Jersey-Tech-Meetup/events/228461491/)
- [Kansas City Golang Meetup](http://www.meetup.com/Kansas-City-Go-lang-Meetup/events/228467750/)
- [Mexico City Gophers](http://www.meetup.com/GophersMX/events/228478343/)
- [Women Who Go London](http://www.meetup.com/Women-Who-Go-London/events/228254901/)

_If your group is not listed here yet, edit the page and add yourself._
_Organisers, once you've added your group, consider tweeting out a link to the page to raise awareness._

### What happens in a release party?
Go 1.6 is the 7th release of the language which has been open source since November 10th, 2009 -- that's 6.5 years since the project was open sourced and nearly 4 years since the 1.0 release.
A lot has changed in the language since 1.0, so this is a great opportunity to discuss the improvements landing 1.6.


#### Go 1.6 slide deck
Here a Go 1.6 presentation slide deck from the Go Sydney users' group. Feel free to use this for your meetup.

[talks.godoc.org/github.com/davecheney/gosyd/go1.6.slide](http://talks.godoc.org/github.com/davecheney/gosyd/go1.6.slide)

_Source_: https://github.com/davecheney/gosyd/blob/master/go1.6.slide

_Please send PR's with corrections/additions_

#### Go 1.6 new and noteworthy

_Please help by expanding this section so meetup organisers can share these details with their groups._

- [Go 1.6 release notes (draft)](http://tip.golang.org/doc/go1.6)
- HTTP/2.

  Go 1.6's `net/http` package supports [HTTP/2](https://http2.golang.org/) for both the client and server out of the box.
  [Here is a video of @bradfitz giving an overview of Go 1.6's HTTP/2 support](https://www.youtube.com/watch?v=gukAZO1fqZQ).
- Garbage Collector improvements.

  Go 1.6 focused heavily on improvements to the low latency collector shipped in Go 1.5.
  Rick Hudson gave a [presentation at GopherCon 2015](https://www.youtube.com/watch?v=aiv1JOfMjm0) describing the low latency collector delivered in Go 1.5, and gave hints to the improvements being worked on for 1.6.
  Rick recently [recorded an interview with InfoQ](http://www.infoq.com/interviews/hudson-go-gc) which focused on 1.6 in more detail.
- GOVENDOREXPERIMENT becomes the default.

  Go 1.5 added experimental support for a mechanism of including the source of your package's dependencies in the package itself, colloquially known as _vendoring_. This feature was opt-in during Go 1.5.
  Go 1.6 makes the vendor support the default, and it's likely that packages will start to use it soon.

- `text/template` changes.
  A long requested ability to [trim whitespace in templates](http://tip.golang.org/pkg/text/template/#hdr-Text_and_spaces) has arrived. This template 

 `"{{23 -}} < {{- 45}}"`

 will produce this output

 `"23<45"` 

- cgo changes

  cgo continues to get stricter about sharing data between Go and C. http://tip.golang.org/cmd/cgo/#hdr-Passing_pointers

  Ian Lance Taylor has put a lot of work into making signal handling more sane. 

- More supported platforms.
  Go 1.6 adds experimental ports to Linux on 64-bit MIPS (linux/mips64 and linux/mips64le). Note that this is 64 bit MIPS, not the older 32 bit MIPS commonly found in routers.

  64-bit PowerPC (linux/ppc64le), Go 1.6 now supports cgo with external linking and is roughly feature complete.

  Go 1.6 also adds an experimental port to Android on 32-bit x86 (android/386). 

_Did you contribute to Go 1.6 and your contribution is not listed here? Edit this page and add some details about what you did._

### What'll happen if Go 1.6 comes out early?
It'll ruin the surprise, but only a little. Being realistic, even without the difficulty of timezones it's impossible to run every meetup at exactly the same time. As mentioned above, Feb 17 is an arbitrary date.

If you're a meetup organiser, Feb 17th would be great, but your participation is more important than being able to organise your group for exactly the 17th.

### What'll happen if Go 1.6 isn't out by the 17th?
Well ... at least we'll have each other. 

The feature set of Go 1.6 isn't going to change in the next few weeks. If Go 1.6 ships after the 17th, it will be a little anticlimactic that we jumped the gun, but it's not a big deal.

### Who's organising this?
Well, if you run a Go meetup, you are. It can't be a worldwide release party without meetups around the globe.

#### No, seriously, who's organising this?
Here are the organisers so far:
- [Dave Cheney](mailto://dave@cheney.net) - @davecheney
- [Carlisia Campos](mailto://carlisia@golangbridge.org) - @carlisia

_Want to help? Edit this page and add yourself_

If you have questions, please reach out to one of the organisers.