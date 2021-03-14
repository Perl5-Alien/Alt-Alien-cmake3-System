# Alt::Alien::cmake3::System ![linux](https://github.com/PerlAlien/Alt-Alien-cmake3-System/workflows/linux/badge.svg)

Simplified alternative to Alien::cmake3 that uses system cmake

# SYNOPSIS

```
env PERL_ALT_INSTALL=OVERWRITE cpanm -n Alt::Alien::cmake3::System
```

# DESCRIPTION

This distribution provides an alternative implementation of Alien::cmake3 that only works with a 
system cmake.  It is intended for testing the core of [Alien::Build](https://metacpan.org/pod/Alien::Build), which includes optional 
tests that use [Alien::cmake3](https://metacpan.org/pod/Alien::cmake3).  The problem with using the real [Alien::cmake3](https://metacpan.org/pod/Alien::cmake3) for testing the 
core of [Alien::Build](https://metacpan.org/pod/Alien::Build) in CI is that [Alien::cmake3](https://metacpan.org/pod/Alien::cmake3) also depends on [Alien::Build](https://metacpan.org/pod/Alien::Build).  This module
may also be useful for system integrators, although I discourage it for that use, as this module may
not be as well supported as the real [Alien::cmake3](https://metacpan.org/pod/Alien::cmake3).

# CAVEATS

The tests use [Test::Alien](https://metacpan.org/pod/Test::Alien) which is now part of the same distribution as [Alien::Build](https://metacpan.org/pod/Alien::Build), so you 
have the same chicken and egg problem.  It is recommended to use the `-n` option on cpanm to skip 
the testing phase.

# AUTHOR

Graham Ollis <plicease@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2018 by Graham Ollis.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
