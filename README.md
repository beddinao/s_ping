# _ping

A minimal command-line tool to test network connectivity by sending ICMP echo requests ("pings") to a specified host and displaying response times, similar to the standard `ping` utility.

---

## Table of Contents

- [Features](#features)
- [Usage](#usage)
- [Example Output](#example-output)
- [Installation](#installation)
- [Requirements](#requirements)
- [Contributing](#contributing)
- [Contact](#contact)

---

## Features

- Sends ICMP echo requests to a target host (domain name or IPv4 address)
- Displays detailed response times for each packet
- Simple, minimal, and fast
- Linux support

---

## Usage

```
./_ping DEST [timeout]
  DEST: domain name/ipv4 address of the target host
  timeout: optional number of seconds until host response
```

---

## Example Output

```
$ ./_ping 1337.ma
1337.ma (104.18.32.248)
	icmp_echo 104.18.32.248 : icmp_echoreply t=55.701 ms, echo.id=13830, icmp_seq=0
	icmp_echo 104.18.32.248 : icmp_echoreply t=58.195 ms, echo.id=13830, icmp_seq=1
	icmp_echo 104.18.32.248 : icmp_echoreply t=32.952 ms, echo.id=13830, icmp_seq=2
	icmp_echo 104.18.32.248 : icmp_echoreply t=20.171 ms, echo.id=13830, icmp_seq=3
	icmp_echo 104.18.32.248 : icmp_echoreply t=27.417 ms, echo.id=13830, icmp_seq=4
	icmp_echo 104.18.32.248 : icmp_echoreply t=21.416 ms, echo.id=13830, icmp_seq=5
^Cquiting..
=== 104.18.32.248 stats ===
packets sent: 7, packet received: 7
time: 1230.085 ms
```

---

## Installation

1. Clone this repository:
   ```sh
   git clone https://github.com/ip-packet/_ping.git
   cd _ping
   ```
2. Build the binary (example for C):
   ```sh
   make
   ```
   _(Or follow language-specific build instructions if provided.)_

3. Run as root (required for raw sockets):
   ```sh
   sudo ./_ping <DEST>
   ```

---

## Requirements

- Linux
- Root privileges (required for sending raw ICMP packets)
- A C compiler and `make` (if building from source)

---


---

## Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## Contact

For questions or support, please open an issue in this repository.

