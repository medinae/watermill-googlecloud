# Watermill Google Cloud Pub/Sub
<img align="right" width="200" src="https://threedots.tech/watermill-io/watermill-logo.png">

[![CircleCI](https://circleci.com/gh/medinae/watermill-googlecloud/tree/master.svg?style=svg)](https://circleci.com/gh/medinae/watermill-googlecloud/tree/master)
[![Go Report Card](https://goreportcard.com/badge/github.com/medinae/watermill-googlecloud)](https://goreportcard.com/report/github.com/medinae/watermill-googlecloud)

This is Pub/Sub for the [Watermill](https://watermill.io/) project.

All Pub/Sub implementations can be found at [https://watermill.io/pubsubs/](https://watermill.io/pubsubs/).

Watermill is a Go library for working efficiently with message streams. It is intended
for building event driven applications, enabling event sourcing, RPC over messages,
sagas and basically whatever else comes to your mind. You can use conventional pub/sub
implementations like Kafka or RabbitMQ, but also HTTP or MySQL binlog if that fits your use case.

Documentation: https://watermill.io/

Getting started guide: https://watermill.io/docs/getting-started/

Issues: https://github.com/ThreeDotsLabs/watermill/issues

## Contributing

All contributions are very much welcome. If you'd like to help with Watermill development,
please see [open issues](https://github.com/ThreeDotsLabs/watermill/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aopen+)
and submit your pull request via GitHub.

### Testing Locally

The tests expect a running instance of PubSub. You can run the emulator specified in the `docker-compose.yml`, then set the correct env variable by running the following:
```
make up
PUBSUB_EMULATOR_HOST=localhost:8085 make test
```

Running one test:

```
make up
PUBSUB_EMULATOR_HOST=localhost:8085 go test -v ./... -run TestPublishSubscribe/TestContinueAfterSubscribeClose
```

## Support

If you didn't find the answer to your question in [the documentation](https://watermill.io/), feel free to ask us directly!

Please join us on the `#watermill` channel on the [Gophers slack](https://gophers.slack.com/): You can get an invite [here](https://gophersinvite.herokuapp.com/).

## License

[MIT License](./LICENSE)
