# Secure Forward (secfwd)

secfwd is a small application that receives TCP/IP connections,
verifies their authenticity against a certificate and then forwards
the connection to another port on success.

## License

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as
published by the Free Software Foundation, either version 3 of the
License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.

## Purpose

To receive a SSL/TSL protected TCP/IP connection, verify the client
certificate and on success, forward the connection to another port.

Also to learn some Go.

## Background

I use a small number of internet exposed services that does not support
SSL client verification, this small application should resolve that.

## Drawbacks

The service behind the this service does not get the remote IP-address,
which could cause problems if this is required.

Not audited for security issues in the implementation itsel, however the
SSL/TLS functionality supplied with Go should be reliable.
