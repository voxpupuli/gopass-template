# gopass secrets Store

## Intro

[gopass](https://www.gopass.pw/) is a neat open source tool for password management.
It handles (GPG) encryption and stores data in a git repo.

## Creating a store

Want a new gopass store like this one? Follow the [instructions in the wiki](https://github.com/voxpupuli/gopass-template/wiki)

## Installation

The upstream docs cover the actual gopass installation: https://github.com/gopasspw/gopass/blob/master/docs/setup.md

## Setup

You will need a valid GPG key.
Validate this with `gpg --list-secret-keys` (please also ensure that it expires after your PMC turn, not during it).

Ask one of the existing admins to add your key to the `.gpg-id` file.
This can be done via [gopass recipients add](https://github.com/gopasspw/gopass/blob/master/docs/commands/recipients.md).

Now you can clone the repo:

```sh
gopass clone git@github.com:voxpupuli/gopass-social.git voxpupuli/social
```

Afterwards `gopass` should have a valid tab completion to list you all the secrets and subcommands.
You can run `gopass ls` to get an overview of all secrets.

To list all GPG keys (people) that have access to the repo, run `gopass recipients`

```terminal
$ gopass recipients
Hint: run 'gopass sync' to import any missing public keys
gopass
├── 0x2b04d7500fe1c6dd15692bb6779eba5eb9d631b8 => 0x779EBA5EB9D631B8 - Sebastian Rakel <sebastian.rakel@service-erp.de>
├── 0x559BEE876892AA5ECD925F28B352E2A17BB89EF5 => 0xB352E2A17BB89EF5 - Ewoud Kohl van Wijngaarden (Red Hat) <ekohlvan@redhat.com>
├── 0x82349A78E7C0B8070B5980FFBA4D1D955112336F => 0xBA4D1D955112336F - Romain Tartière <romain@nfc-tools.org>
├── 0x83CE67EC15FA9327838924766CE2B38A165F224B => 0x6CE2B38A165F224B - Robert Waffen <rw@betadots.de>
├── 0xC10B6298A584A5632E254DA304D659E6BF1C4CC0 => 0x04D659E6BF1C4CC0 - Tim Meusel <tim@bastelfreak.de>
└── 0xEA338528809E9749E2C3064379E924EBEDA7F3FD => 0x79E924EBEDA7F3FD - Alexander John Fisher <alex@linfratech.co.uk>
```

## Common commands

There is a nice cheat sheet at [woile.github.io/gopass-cheat-sheet](https://woile.github.io/gopass-cheat-sheet/).
