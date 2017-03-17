# SPI

This gem aims to provide a Unified method of talking to SPI devices on a variety of hardware. This is mainly aimed at a range of Small Board Computers (SBCs) such as the Raspberry Pi and C.H.I.P. computers.

Currently only the Linux spidev kernel interface is implimented however the code is designed to make adding other drivers a simple process. It should then be possible to choose the correct driver for the hardware without having to re-write code.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'spi'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install spi

## Usage

You may need to enable the SPI device on your hardware and/or load the kernel module.
On the Raspberry Pi SPI can be enabled through raspi-cofig
On the C.H.I.P. SPI can be loaded by importing the SPI DTB

After doing this you should find one or more devices in /dev
```bash
user@device:~ $ ls /dev/spi*
/dev/spidev32766.0
```


Currently there's only one Driver (SPI::Driver::SPIdev) and it takes a device parameter.

TODO: Write usage instructions here


## Development

After checking out the repo, run `bin/setup` to install dependencies. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/spi.
