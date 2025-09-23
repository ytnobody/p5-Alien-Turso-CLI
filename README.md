
# NAME

Alien::Turso::CLI - Install and find Turso CLI

# SYNOPSIS

    use Alien::Turso::CLI;
    use Alien qw( Alien::Turso::CLI );
    
    my $turso = Alien::Turso::CLI->bin_dir . '/turso';
    system $turso, "--version";

# DESCRIPTION

Alien::Turso::CLI provides the Turso CLI (Command Line Interface) for Perl applications.
This module will download and install the Turso CLI binary if it's not already available on your system.

Turso CLI is the official command-line interface for Turso, the edge-hosted, distributed database built on libSQL.

## REQUIREMENTS

- Perl 5.18 or later
- Linux x86_64 platform (currently supported)
- Internet connection for downloading Turso CLI binary

## INSTALLATION

    cpanm Alien::Turso::CLI

Or manually:

    perl Build.PL
    ./Build
    ./Build test
    ./Build install

After installation, you can use the Turso CLI:

    perl -MAlien::Turso::CLI -E 'system Alien::Turso::CLI->bin_dir . "/turso", "--version"'

## KNOWN ISSUES

During installation, you may see warnings about "Download::Negotiate" plugin. 
These warnings are harmless and do not affect functionality. They are a known 
issue with the current version of Alien::Build::Plugin::Download::GitHub, 
which correctly uses the GitHub API despite the warnings.

# LICENSE

Copyright (C) ytnobody.

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# AUTHOR

ytnobody <ytnobody@gmail.com>
