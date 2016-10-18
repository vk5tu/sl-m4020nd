# PPD for Samsung SL-M4020ND monochrome duplex laser printer.

The Samsung SL-M4020ND is a laser printer which does black-and-white
printing on both sides of the paper. It has USB and ethernet
interfaces. It supports the PCL, PostScript and PDF printing
languages.

This PPD is reverse-engineered from connecting with the printer and
querying its capabilities.

Hopefully it gives a better result than some other PPD files for this
printer. In particular the lack of guesswork should lead to less time
spent in CUPS filters.

Feedback is welcome, create an issue at the [Github repository](https://github.com/vk5tu/sl-m4020nd/issues).

## Installation

To install the PPD on Linux open your web browser to http://localhost:631/

It will ask for a userid and and password, and the "root" user would
often be appropriate.

Select *Administration*, then *Add Printer*, then *Internet Printing Protocol (http)*. Press *Continue*.

When asked for the *Connection* give the printer's IPP name in this format *http://printer.example.com:631/ipp/print*, replacing "printer.example.com" with a DNS name, or a IPv4 address, or a IPv6 address between square brackets. Press *Continue*.

Provide the printer's *Name* and *Description*. It's best if these are the same and are single-world and lower-case; say `sl-m4020nd`. Provide the *Location*. Don't *Share this printer*. Press *Continue*.

When prompted to *Provide a PPD file* then press *Choose file*, select `saslm402.ppd` from ~/Downloads or whereever you cloned this repository to. Press *Add printer*.

-glen
