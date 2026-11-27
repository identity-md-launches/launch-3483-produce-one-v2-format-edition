OPEN INTEREST / Daily brief, format v2. Friday, 27 November 2026.

LEAD: An attacker rerouted bitcoin miners' traffic and took up to 1.9 EH/s of hashrate.

Braiins reported on 25 November 2026 that an imposter pool captured miners on unencrypted Stratum V1 connections. The pool says the attack is still live and that fixes already exist. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1]

Braiins says the attacker rerouted internet traffic between miners and pools, impersonated the pool and handed miners its own work. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1] Neither the machines nor Braiins Pool were breached, according to the report. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1]

The episodes grew quickly. Braiins counted 19 episodes in Latin America from 7 to 12 November 2026, each hitting 120 to 400 sites and 36 to 174 PH/s. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1] On 20 November 2026, four episodes in mostly European networks hit 1,050 to 1,600 sites and up to 1.9 EH/s, lasting 6 to 49 minutes. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1]

The first sign was a share difficulty of 536,870,912 on three Antminer S19s in Brazil. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1] The machines kept hashing at full speed while their pool dashboards showed zero. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1] Braiins says every affected miner received a network reset in the same second and reconnected to the same hostname and IP address, so DNS was untouched. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1]

The weakness is old. Stratum V1 sends everything in plain text and gives a miner no way to check who is on the other end, a fact since 2012. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1] Braiins cites a 2014 Dell SecureWorks case in which the same routing trick took about $83,000 in rewards. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1]

The exposure is wide. Braiins says public routing data shows the technique aimed at address blocks hosting the Stratum endpoints of most large pools. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1] Any pool address beginning with stratum+tcp://, backups included, can be hijacked. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1]

Braiins did not estimate the rewards taken, and the attacker is unnamed. [https://www.theblock.co/news/ecosystems/2026-11-25-bitcoin-miners-hit-hashrate-hijacking-attack-exploiting-unencrypted-connections-446723] The Block quotes the pool reading the growth as "testing the waters." [https://www.theblock.co/news/ecosystems/2026-11-25-bitcoin-miners-hit-hashrate-hijacking-attack-exploiting-unencrypted-connections-446723]

NEWS:

[NEWS] Chainflip says an attacker took $12.6 million with signatures the network never requested.
Chainflip Labs said on 23 November 2026 that an attacker emptied its Bitcoin and Ethereum vaults on 21 November 2026. [https://chainflip.io/blog/incident-report-vault-exploit-21-november-2026-part-1] The haul was 133.34 BTC plus 520.22 ETH, 3,249,631 USDC and 758,141 USDT, effectively the entire vault balance. [https://chainflip.io/blog/incident-report-vault-exploit-21-november-2026-part-1] The team says a registered but inactive validator account, cFMH2YX722cFGNemZ5tbZnq7XvYZ3xWyTRdLrW1cLgyrJtEKe, used peer access to exploit a memory-safety flaw in a third-party networking library and extract key shares. [https://chainflip.io/blog/incident-report-vault-exploit-21-november-2026-part-1] Chainflip says some steps of that account are not yet confirmed, and that 2,909 ETH went into Tornado Cash. [https://chainflip.io/blog/incident-report-vault-exploit-21-november-2026-part-1]

[NEWS] The European Commission proposes a crypto blockade on Kyrgyzstan.
Ursula von der Leyen presented the 22nd sanctions package against Russia on 23 November 2026. [https://cyprus.representation.ec.europa.eu/news/statement-president-von-der-leyen-22nd-package-sanctions-against-russia-2026-11-23_en] She said it targets crypto and payment networks, including third countries that help Russia evade sanctions, and extends a transaction ban to some 60 Russian banks. [https://cyprus.representation.ec.europa.eu/news/statement-president-von-der-leyen-22nd-package-sanctions-against-russia-2026-11-23_en] The Kyiv Independent reports that the plan activates a 21st-package tool against Kyrgyzstan, which an unnamed EU official called dismissive of the bloc's overtures. [https://kyivindependent.com/eu-proposes-package-of-russian-sports-sanctions-visa-bans-and-a-krygyzstan-crypto-blockade/] Adoption needs all 27 member states. [https://crypto.news/eu-kyrgyzstan-crypto-exchange-sanctions/]

[NEWS] Auditors find about 15,000 Ethereum contracts that Glamsterdam's gas change would break.
ChainSecurity and Dedaub presented audit results on mainnet contracts affected by EIP-8037, according to Ethlabs' Derek Chiang on 22 November 2026. [https://ethlabs.org/updates/week-22.html] Chiang reports about 15,000 of 90 million contracts are affected, or 0.016%, holding about $500,000. [https://ethlabs.org/updates/week-22.html] Most break because they hardcode gas numbers, and a small minority because of the new state gas reservoir. [https://ethlabs.org/updates/week-22.html] Chiang says the issue has put Glamsterdam behind schedule. [https://ethlabs.org/updates/week-22.html]

TECH:

[TECH] Ethlabs recommends shipping Glamsterdam with its state repricing intact.
Caspar Schwarz-Schilling wrote on 25 November 2026 that Ethlabs backs Glamsterdam as is, calling the problems found "serious and valid." [https://ethlabs.org/writings/glamsterdam-position.html] He argues that removing EIP-8037 would forfeit the fork's roughly 3x higher gas limit and only postpone the problem. [https://ethlabs.org/writings/glamsterdam-position.html] He adds that any change now costs months, and that Sepolia has already forked with the old version. [https://ethlabs.org/writings/glamsterdam-position.html] His lessons: flag disruptive changes early and bring application developers in sooner. [https://ethlabs.org/writings/glamsterdam-position.html]

[TECH] Braiins ships three fixes for plain-text mining connections.
Braiins says the remedy is Stratum V2, or Stratum V1 over TLS on firmware that verifies the pool's certificate. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1] For miners that can do neither, it released a small proxy to run inside the miner's own network on 25 November 2026. [https://braiins.com/blog/bitcoin-hashrate-hijacking-unencrypted-stratum-v1] The pool wrote in 2020 that V2's encryption and relay authentication would make this attack impossible, a vendor claim rather than an independent audit. [https://braiins.com/blog/hashrate-robbery-stratum-v2-fixes-this-and-more]

CULTURE:

[CULTURE] An Ethereum core developer says the next forks are about making ETH a store of value.
Derek Chiang wrote on 22 November 2026 that core developers "hold ETH too" and feel responsible when markets fall. [https://ethlabs.org/updates/week-22.html] He frames Glamsterdam as scaling without hurting decentralisation, and Hegota as protecting the chain against quantum computers and AI. [https://ethlabs.org/updates/week-22.html] He argues ETH's value as a store of value depends on decentralisation rather than fee revenue. [https://ethlabs.org/updates/week-22.html]

[CULTURE] Molly White says the downturn has buried the bitcoin-as-hedge story.
In her 24 November 2026 issue, White wrote that bitcoin fell below $56,000, its lowest since September 2024, as the Nasdaq dropped more than 5%. [https://www.citationneeded.news/issue-112/] She argued that bitcoiners long sold it as a hedge against stocks, yet it fell alongside tech shares and did not bounce back with them. [https://www.citationneeded.news/issue-112/] She also cites a JPMorgan estimate that mining one bitcoin costs about $86,000, well above the current price. [https://www.citationneeded.news/issue-112/]

READING LIST:
[https://www.citationneeded.news/crypto-ai-lost-the-midterms/] Molly White's 13 November 2026 tally of how crypto and AI super PACs fared in competitive races.
[https://ethlabs.org/writings/tracking-glamsterdam.html] Ethlabs' running account of the fork this edition covers in two items.
[https://braiins.com/blog/hashrate-robbery-stratum-v2-fixes-this-and-more] The 2020 Braiins warning that this edition's lead turned from theory into incident.
[https://eur-lex.europa.eu/eli/reg/2026/1848/oj] The regulation text holding the country-wide crypto tool the Commission now proposes to use.

METHOD:
The sweep ran from 25 November 2026 to 10:30 UTC on 27 November 2026 across pool and protocol blogs, Commission statements, incident reports and the masthead's own sites. Rotation used editions 010 through 012, and no voice or outlet they cited appears here. Ethlabs is the masthead entry for Barnabé Monnot; Molly White is a masthead voice. The ChainSecurity and Dedaub figures rest on Ethlabs' secondary account, as the audits themselves were not opened. The Kyrgyzstan detail rests on the Kyiv Independent and crypto.news, attributed by name, because the Council annexes were not reachable. The Braiins attack data is the pool's own and has no independent confirmation. Cut for failed verification: a 26 November 2026 South Korean draft law capping exchange ownership, a Lighter exploit and an ESMA registry timeline.
