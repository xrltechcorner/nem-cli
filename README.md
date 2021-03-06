# evias/nem-cli

nem-cli is a collection of command line tools useful when working with the NEM Blockchain using the Terminal.

This package aims to provide an easy to use Command Line Tools Suite for the NEM Blockchain. 

The NEM Blockchain provides features including: cryptocurrency wallets and transactions, a custom cryptocurrency tokens platform, namespaces management on the blockchain, multi signature accounts out-of-the box and also voting features.

The command line tools suite is built such that each script/command can be run in a single process using UNIX terminals. (A wrapper for MS Windows will be written soonish)

Feel free to contribute wherever you think you can help! NEMazing ideas much appreciated!

## Download & Installation

Run the following from the terminal:

```bash
$ git clone git@github.com:evias/nem-cli.git nem-cli/
$ cd nem-cli
$ npm install

# and to make it more comfortable
$ echo "alias nem-cli='./nem-cli'" >> ~/.bashrc 
$ source ~/.bashrc
```

You are now all set and you can use the nem-cli Package as described in the Usage section.

## Usage

There is multiple ways to interact with this command line tools suite. You can use `npm` to start your instance the CLI and you can specify options, command and arguments to your command line call.

Here is a write-up of some examples for running the `nem-cli` command line tools suite:

```bash
$ nem-cli list
$ nem-cli api [arguments]
$ nem-cli wallet [arguments]
$ nem-cli --help
```

or 

```bash
$ npm start list
$ npm start api  [arguments]
$ npm start wallet  [arguments]
```

.. or

```bash
$ ./babel-node nem-cli list
$ ./babel-node nem-cli api [arguments]
$ ./babel-node nem-cli wallet [arguments]
$ ./babel-node nem-cli --help
```

## Examples

Following examples apply for the `nem-cli` command line tools suite:

```bash
$ nem-cli list
$ nem-cli api --help

# Simples use case (Current chain height)
$ nem-cli api --url /chain/height
$ nem-cli api --url /chain/height --network mainnet

# POST request example and GET with parameters
$ nem-cli api --url /block/at/public --post --json '{"height":1149971}'
$ nem-cli api --url /account/get?address=TDWZ55R5VIHSH5WWK6CEGAIP7D35XVFZ3RU2S5UQ

# Compare Chain Heights by switching Nodes:
$ nem-cli api --url /chain/height --node bigalice2.nem.ninja
$ nem-cli api --url /chain/height --node alice6.nem.ninja
$ nem-cli api --url /chain/height --node b1.nem.foundation --port 7895

# Use the headless wallet features
$ nem-cli wallet --address TDWZ55R5VIHSH5WWK6CEGAIP7D35XVFZ3RU2S5UQ --overview
$ nem-cli wallet --address TDWZ55R5VIHSH5WWK6CEGAIP7D35XVFZ3RU2S5UQ --watch

# Use a simple terminal menu to interact with wallet
$ nem-cli wallet --file /home/you/Downloads/your.wlt
$ nem-cli wallet --address TDWZ55R5VIHSH5WWK6CEGAIP7D35XVFZ3RU2S5UQ
```

NE{m}njoy! :)

## Pot de vin

If you like the initiative, and for the sake of good mood, I recommend you take a few minutes to Donate a beer or Three [because belgians like that] by sending some XEM (or whatever Mosaic you think pays me a few beers someday!) to my Wallet:

    NCK34K5LIXL4OMPDLVGPTWPZMGFTDRZQEBRS5Q2S

## License

This software is released under the MIT License.

© 2017 Grégory Saive greg@evias.be, All rights reserved.
