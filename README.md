# Panasonic Let's Note SX4 Project

This repo tracks the restoration, upgrades, sourcing, and Linux setup for a Panasonic Let's Note CF-SX4.

## Current machine

- **Model:** Panasonic Let's Note CF-SX4
- **Exact SKU:** CF-SX4FDDBP
- **CPU:** Intel Core i7-5600U
- **Display:** 12.1-inch, 1600×900
- **RAM:** 24 GB total
  - 8 GB onboard
  - 16 GB DDR3L SO-DIMM installed
- **Storage:** 1TB Sandisk SSD installed
- **Original HDD:** preserved intact with the original Panasonic Windows install
- **Optical drive:** present, but faulty
  - spins/tries to read a disc three times, then gives up
- **Power input:** 16 V barrel input
- **OS plan:** English Windows for testing, with Zorin OS under consideration for daily use

## Completed work

- Installed SATA SSD
- Installed 16 GB DDR3L SO-DIMM
- Confirmed Windows sees **24 GB RAM**
- Preserved the original HDD and factory Windows installation
- Confirmed the optical drive has a read/spin failure
- Ordered a replacement 16 V power brick

---

# Bill of Materials

| Priority | Item | Target part / spec | Market target | Status | Notes |
|---|---|---|---:|---|---|
| 1 | USB-C PD power cable | **PDQC PDC-15VE-5525A** | **¥1,780** | Planned | 1.5 m, 5.5×2.5 mm barrel, 15 V trigger cable with e-marker. Use with ≥65 W PD charger. |
| 1 | Optical drive | **Panasonic/MATSHITA UJ8B9A** (UJ8B9 family), confirmed SX4-compatible | **~¥1,440–¥1,680 used/tested** | Needed | Exact mechanism identified from this machine. Buy the UJ8B9A version, not DP-8A4SH. Verified-used units regularly appear in Japan. |
| 2 | Large battery | **CF-VZSU76JS** | **~¥11,420–¥11,465 new** | Optional | Silver large-capacity 8-cell battery. |
| 2 | Small battery | **CF-VZSU75JS** | **~¥6,999 new** | Optional | Silver lightweight battery. |
| 2 | Genuine AC adapter | **CF-AA6412C / CF-AA6412CJS**, 16 V 4.06 A | **~¥1,300–¥2,000 used** | Optional | Useful as a known-good OEM reference supply. |
| 3 | USB-C charger | 65–100 W GaN USB-C PD | **$35–$70** | Optional | Must expose a suitable 15 V PD profile. |
| 3 | Spare PD trigger | Let’s Note 15 V 5.5×2.5 mm trigger adapter | **~¥850–¥1,700** | Optional | Handy spare, but verify output profile before use. |

---

# Current market snapshot

**Important:** these are observed Japanese-market prices and recent sale/listing comps, not guaranteed live stock. Verify the listing before buying.

## Optical-drive market

The optical mechanism in this machine has now been positively identified from the label inside the SX4 as:

- **Panasonic UJ8B9A**
- family/model reported by Windows as **MATSHITA DVD-RAM UJ8B9**
- sticker observed in this machine: `UJ8B9A / BCD1-A / 5FFWE`

Yahoo Auctions Japan currently has several auctions for this drive: **tested UJ8B9A drives explicitly advertised for CF-SX1 / CF-SX2 / CF-SX3 / CF-SX4** at about:

- **¥1,440 Buy It Now + ¥185 domestic shipping**
- seller description: **tested with four kinds of media**
- repeated listings from the same 100%-feedback Tokyo seller suggest this is a recurring stocked part rather than a one-off donor pull

Recent completed examples from the same seller also sold for **¥1,440**, while older completed listings were around **¥1,680**.

Historical confirmation also exists from an SX4 owner who bought a used **UJ8B9** for **¥2,453 shipped** and successfully restored DVD playback.

### Buying target

- **Excellent:** ¥1,400–¥1,700 tested UJ8B9A
- **Fine:** up to about ¥2,500 if explicitly read-tested and complete
- **Avoid:** untested UJ8B9A unless nearly free
- **Do not substitute:** **DP-8A4SH** — SX-series machines used both mechanisms and the surrounding mechanical structure differs

A full donor SX4 is now **optional**, not the primary DVD-repair strategy. It is still useful for spare chassis parts, keyboard pieces, hinges, fan, cables, etc., but it is unnecessary just to fix the optical drive.

## Optical drive notes

The SX4 uses Panasonic's unusual **cover-style / shell-drive** arrangement, but the optical mechanism itself is replaceable.

### Exact mechanism in this machine

**Panasonic UJ8B9A**

The label inside this SX4 reads:

- `Panasonic`
- `UJ8B9A`
- `BCD1-A`
- `5FFWE`

The UJ8B9A is a known Let's Note SX-series mechanism. Multiple sources document successful replacement in SX-series machines, including an SX4 replacement using a UJ8B9-family unit.

### Important compatibility warning

The SX series was built with at least two mechanically different optical-drive families:

- **UJ8B9 / UJ8B9A**
- **DP-8A4SH**

They are **not drop-in interchangeable** because Panasonic changed the surrounding mechanical structure to match the drive type.

This machine is confirmed **UJ8B9A**, so replacement shopping should be restricted to UJ8B9/UJ8B9A units specifically advertised for the SX1/SX2/SX3/SX4.

Useful search terms:

- `UJ8B9A`
- `UJ8B9`
- `CF-SX4 UJ8B9A`
- `CF-SX4 UJ8B9`
- `Panasonic CF-SX1 CF-SX2 CF-SX3 CF-SX4 UJ8B9A`
- `レッツノート UJ8B9A`
- `CF-SX4 DVDドライブ UJ8B9`

## Battery

### Large silver battery — CF-VZSU76JS

- 7.2 V, 8-cell
- nominal capacity: 13,600 mAh
- rated capacity: 12,800 mAh
- weight: about 430 g
- observed new-retail pricing: **~¥11,420–¥11,465**

### Small silver battery — CF-VZSU75JS

- lightweight silver battery for SX-series machines
- observed Japanese retail pricing: **~¥6,999**

For this project, the **CF-VZSU76JS** is preferred if runtime matters more than minimum weight.

## Genuine AC adapter

Useful OEM reference:

- **CF-AA6412C / CF-AA6412CJS**
- Output: **16 V / 4.06 A**
- Recent Mercari pricing observed around **¥1,300–¥2,000 used**

A genuine adapter is worth keeping even if USB-C PD becomes the normal power source.

## USB-C PD conversion

### PDQC PDC-15VE-5525A

- Price observed: **¥1,780**
- USB-C PD trigger cable
- 15 V output
- 5.5×2.5 mm barrel plug
- 1.5 m cable
- e-marker present
- cable is capable of 5 A
- recommended with a **65 W or greater** USB-C PD source
- many chargers only provide **15 V / 3 A**, so a stronger 15 V profile is preferable

PDQC notes that some Let's Note systems may show a non-genuine AC adapter warning.

### Do not use

Avoid generic fixed **20 V** USB-C-to-barrel cables. The SX4 expects a 16 V-class supply.

---

# Known issues

## Slow Panasonic-logo POST

The machine spends a long time at the Panasonic splash screen before boot.

This behavior existed **before** the 16 GB SO-DIMM upgrade, so the 24 GB RAM configuration is not currently considered the cause.

Current suspects:

1. failing optical drive / firmware timeout
2. boot-order delay
3. PXE/network boot probing
4. stale firmware configuration
5. aging RTC/CMOS battery

### Planned POST test

1. Boot normally and time Panasonic-logo duration.
2. Remove optical drive from boot order.
3. Disable PXE/network boot.
4. Test without USB devices or SD card.
5. If possible, electrically disconnect the optical drive and repeat the test.
6. Compare timing.

If POST becomes dramatically faster with the optical drive disconnected, the failed shell drive is likely causing a firmware enumeration timeout.

---

# Linux plan

Current leading choice: **Zorin OS**

Other candidates:

1. Linux Mint Cinnamon
2. Zorin OS
3. Fedora Workstation
4. Ubuntu LTS
5. Debian + XFCE
6. Fedora XFCE
7. Arch + KDE Plasma

Things to test from a live USB:

- Wi-Fi
- Bluetooth
- audio
- brightness keys
- sleep/resume
- touchpad
- battery reporting
- optical-drive behavior
- SD reader
- HDMI/VGA output
- fan behavior and thermals

---

# Parts sourcing plan

## Next Sendico shipment

Preferred order:

1. **PDQC PDC-15VE-5525A**
2. **Tested UJ8B9A optical drive for CF-SX1/SX2/SX3/SX4**
3. **CF-VZSU76JS** if a genuinely new or healthy pack appears at a reasonable price
4. Optional **genuine CF-AA6412C/CF-AA6412CJS**
5. Small Panasonic-specific spare parts if shipping consolidation makes them effectively free

## Search strategy

For the optical-drive repair, a tested UJ8B9A is now preferable to a full junk donor. A donor machine is still useful for non-drive mechanical spares.

Priority search terms:

- `UJ8B9A`
- `UJ8B9`
- `CF-SX4 UJ8B9A`
- `CF-SX4 DVD UJ8B9`
- `CF-SX4 部品取り`
- `CF-SX4 ジャンク`
- `CF-VZSU76JS`
- `CF-AA6412C`
- `レッツノート PD 5525 15V`

---

# Reference links

- PDQC PDC-15VE-5525A  
  https://pdqc.net/items/65f3e08524c2f40906b248e7

- Yahoo Auctions search for tested UJ8B9A (CF-SX1/SX2/SX3/SX4)  
  https://auctions.yahoo.co.jp/search/search/cf-sx4%20note/0/

- Yahoo Auctions completed-price reference for UJ8B9A  
  https://auctions.yahoo.co.jp/closedsearch/closedsearch?auccat=23412&b=1&brand_id=101460&dest_pref_code=12&fixed=0&max=1634&min=1090&mode=3&n=100&price_type=currentprice&select=6

- Successful CF-SX4 UJ8B9 replacement write-up  
  https://lazycatumezawa.blog.fc2.com/blog-category-16.html

- Mercari UJ8B9A listing showing UJ8B9 vs DP-8A4SH incompatibility  
  https://jp.mercari.com/item/m43019968018

- SX2 UJ8B9A replacement write-up  
  https://blog.simoyan.jp/2019/08/25_1032467359.html

- Panasonic SX/NX option compatibility page  
  https://ec-plus.panasonic.jp/store/page/pc/option/

- Panasonic CF-SX4 driver/support page  
  https://ask-pc-support.connect.panasonic.com/dl/install/sx4h.html

- Panasonic shell-drive emergency-open documentation  
  https://faq-pc-support.connect.panasonic.com/faq/show/164

- CF-VZSU76JS pricing reference  
  https://review.kakaku.com/review/K0000395463/

- Yahoo Auctions CF-SX4 junk completed-auction comps  
  https://auctions.yahoo.co.jp/closedsearch/closedsearch/cf-sx4%20%E3%82%B8%E3%83%A3%E3%83%B3%E3%82%AF/0/

- Mercari CF-SX4 search  
  https://jp.mercari.com/search?keyword=Panasonic%20CF-SX4

---

# Notes

This machine is already well beyond its typical original configuration:

- SSD instead of the original hard drive
- 24 GB RAM successfully recognized by Windows
- potential USB-C PD conversion
- Linux daily-driver plan
- restoration of the distinctive Panasonic shell-drive optical system

The goal is to keep the machine useful while preserving the weird, compact, highly serviceable character that makes the SX4 interesting in the first place.
