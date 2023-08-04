<h1 align="center">
  <br>
  Pion simulnet
  <br>
</h1>
<h4 align="center">A net implementation that enables simulations</h4>
<p align="center">
  <a href="https://pion.ly"><img src="https://img.shields.io/badge/pion-simulnet-gray.svg?longCache=true&colorB=brightgreen" alt="Pion "></a>
  <a href="https://sourcegraph.com/github.com/pion/simulnet?badge"><img src="https://sourcegraph.com/github.com/pion/rtp/-/badge.svg" alt="Sourcegraph Widget"></a>
  <a href="https://pion.ly/slack"><img src="https://img.shields.io/badge/join-us%20on%20slack-gray.svg?longCache=true&logo=slack&colorB=brightgreen" alt="Slack Widget"></a>
  <br>
  <img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/pion/simulnet/test.yaml">
  <a href="https://pkg.go.dev/github.com/pion/simulnet"><img src="https://pkg.go.dev/badge/github.com/pion/simulnet.svg" alt="Go Reference"></a>
  <a href="https://codecov.io/gh/pion/simulnet"><img src="https://codecov.io/gh/pion/simulnet/branch/master/graph/badge.svg" alt="Coverage Status"></a>
  <a href="https://goreportcard.com/report/github.com/pion/simulnet"><img src="https://goreportcard.com/badge/github.com/pion/simulnet" alt="Go Report Card"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
</p>
<br>

`simulnet` aims to make testing how your software and hardware perform in adverse network conditions easier. Originally used to test [Google Congestion Control](https://github.com/pion/interceptor/tree/master/pkg/gcc),
but designed to be generally useful.

For Go users a [net](https://pkg.go.dev/net) implementation is provided. For non-Go users it can be used via TUN/TAP. Your application can listen on the TUN/TAP interface and
doesn't need to be modified. simulnet then provides two set of APIs to influence the network.

The first is a imperative API to influence the state of the network allowing you to set things like.
* Packets Per Second
* Bytes Per Second
* Overuse Behavior
* Packet Loss
* Delay

The second is a declarative API where you provide a list of rules.
* Modify Bytes Per Second to be between 800 and 1500 every 30 seconds
* Set Packet Loss to 5% for 2 seconds every 5 minutes

simulnet will announce when modifications are made to the network. Then you can easily
understand what network condition in particular caused your software to fail/have problems.

### Using

### Contributing
Check out the **[contributing wiki](https://github.com/pion/webrtc/wiki/Contributing)** to join the group of amazing people making this project possible:

### License
MIT License - see [LICENSE](LICENSE) for full text
