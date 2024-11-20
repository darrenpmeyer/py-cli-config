py-cli-config for Python 3
==========================

An opinionated configuration system and argument parser for Python 3 CLI applications

See `cli_config`_ module folder for installation and other details.

.. _cli_config: cli_config/

Philosophy -- why another one of these?
---------------------------------------

So many argument systems for CLIs either try to be a full CLI framework, which is overkill for many applications, or they try to be so flexible that declaring options/arguments requires a lot of design decision and fussing about.

It's my belief that managing configuration for a CLI should be simple and straightforward, making the most common use cases easy. Therefore the goal is to be able to declare a configurationn template, and then:

- load configuration files from a list of paths, with sensible "override" rules (local dir settings overriding system dir settings, for example)
- override configuration items for a given run using environment variables
- automatically generate command-line switch definitions so you can override configuration that way (while allowing for overriding the automatic choices)

I *don't* want:

- too many choices for option syntax
- a system that forces you to do everything through declaration only (you should write python code to do complex things)