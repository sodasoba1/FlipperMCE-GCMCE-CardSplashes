# FlipperMCE-GCMCE-CardSplashes

SD Card layout for FlipperMCE/GCMCE card splash `.bin` files (OLED images).

## Quick Start
This repository provides a pre-configured `.bin` and `.ini` file structure for a basic SD card setup. 

> [!IMPORTANT]
> I strongly recommend reading the official documentation at [flippermce.github.io](https://flippermce.github.io/) before starting.

## Regional Syncing & Automation
To provide maximum compatibility across libraries, this collection uses an automated "Master Template" system:
* **Primary Source:**  splashes are created for the **NTSC-U (USA)** region.
* **Cross-Region Compatibility:** Using Python automation, these USA assets are synced across **PAL (EUR/UKV)** and **NTSC-J (JPN)** folders.
* **Redundancy:** Each folder includes both the primary `.bin` and a `-1.bin` redundancy file to ensure the splash displays correctly regardless of your file naming convention.

## Image Sources & Processing
Original images (before conversion) are located in `/CardSplashes-prebin`. 
* **Enhancements:** Many images have been manually edited to improve contrast, crispness, and legibility on small OLED screens.
* **Conversion:** Files were generated using the [FlipperMCE Splash Generator](https://flippermce.github.io/splashgen/splashgen.html).

# ID - DB
[Game ID & Serial DB](https://sodasoba1.github.io/FlipperMCE-GCMCE-CardSplashes/)

# GameCube Translation / ROM Notes

---

## Translation with Header Changed (NO CARD / BIN / RAW LOADS)

| JP ID | JP Title | EN ID | EN Title |
|------|----------|-------|----------|
| GAEJ01 | どうぶつの森 e+ | GAEE01 | Animal Forest e+ |
| GY3J01 | ドンキーコンガ 3 食べ放題！春もぎたて50曲 | GY3E01 | Donkey Konga 3 |
| GC4JBN | 新世紀GPXサイバーフォーミュラ Road To The Evolution | GC4EBN | Cyber Formula -Road To The EVOLUTION- |
| GKQJ01 | くるりんスカッシュ！ | GKQE01 | Kururin Squash! |
| GXQF41 | Taxi 3 | GXQP41 | Taxi 3: The Game |
| GL3JE8 | ルパン三世：海に消えた秘宝 | GL3EE8 | Lupin III: Lost Treasure Under the Sea *(see Additional)* |
| PGSJ01 | メタルギア -Special Disc- | PGSE01 | Metal Gear Solid: The Twin Snakes: Special Disc |
| G4NJDA | NARUTO -ナルト- 激闘忍者大戦！4 | SG4JDA | Naruto: Clash of Ninja 4 *(header very different)* |
| GPZJ01 | NINTENDO パズルコレクション | GPZE01 | Nintendo Puzzle Collection |
| GABJB2 | 金色のガッシュベル!! ゴー!ゴー!魔物ファイト!! | GZBEB2 | Zatch Bell! Go! Go! Mamodo Fight!! |

---

## Translation with NO Header Change (SAVE GAME LOADS / WORKING)

| ID | JP Title | EN Title |
|----|----------|----------|
| GD5JB2 | ドラゴンドライブ ディマスターズショット | Dragon Drive - D-Masters Shot |
| GHEJ91 | ホームランド | HomeLand |
| GRWJD9 | スーパーロボット大戦 GC | Super Robot Wars GC |
| GDPJAF | ミスタードリラー ドリルランド | Mr. Driller: Drill Land |
| GLJJMS | ラジルギ ジェネリック | Radirgy Generic |
| GZVJDA | ゾイド バーサスⅢ | Zoids Vs. III |
| GBRJ18 | ブラッディ ロア エクストリーム | Bloody Road Extreme |

---

## ROM Hacks:


### Super Mario Sunshine

- GMSE01 → Super Mario Sunshine  
  - GMSE03 → Super Mario Sunburn  
    - Uses Channel 2 → `DL-DOL-GMSE-USA-2.raw/bin`
  - GMSE04 → Super Mario Eclipse  
    - Uses Channel 3 → `DL-DOL-GMSE-USA-3.raw/bin`

**SD Location:** `FlipperMCE/GCMCE`

#### Config
`SD:/MemoryCards/DL-DOL-GMSE-USA/Card1.ini`

```ini
[ChannelName]
1=Super Mario SunShine
2=Super Mario SunBurn
3=Super Mario Eclipse
4=UNUSED

[Settings]
MaxChannels=4
CardSize=64
```

---


 ### Mario Kart: Double Dash

- GM4E01 → Mario Kart: Double Dash!!  
  - GM4E64 → Mario Kart Double Dash!! Plus v2.0 
    - Uses Channel 2 → `DL-DOL-GM4E-USA-2.raw/bin`
  - GM4E64 → M64 MKDD Extended v2.0  
    - Uses Channel 3 → `DL-DOL-GM4E-USA-3.raw/bin`
	
**SD Location:** `FlipperMCE/GCMCE`

##### Config

`SD:/MemoryCards/DL-DOL-GM4E-USA/Card1.ini`

```ini
[ChannelName]
1=Mario Kart: Double Dash!!
2=Mario Kart: Double Dash!! Plus
3=M64 MKDD Extended v2.0
4=UNUSED
[Settings]
MaxChannels=4  # Maximum number of channels for this card
CardSize=64
```

**SD Location:** `SD2SP2/SDGECKO/Swiss Location`

`SD:/Swiss/settings/game/GM4E.ini`

```
# Game specific configuration file. Created by Swiss
ID=GM4E
Name=M64 MKDD Extended v2.0
Comment=No Comment
Status=Unknown
```

---

### Pokemon XD: Gale of Darkness

- GXXE01 → Pokemon XD: Gale of Darkness 
  - GXXE01 → Pokemon XD: Gale of Darkness: Equality Version
    - Uses Channel 2 → `DL-DOL-GXXE-USA-2.raw/bin`
  - GXXE01 → Pokemon XG: NeXt Gen 
    - Uses Channel 3 → `DL-DOL-GXXE-USA-3.raw/bin`

**SD Location:** `FlipperMCE/GCMCE`

`SD:/MemoryCards/DL-DOL-GXXE-USA/Card1.ini`

```
[ChannelName]
1=Pokemon XD: Gale of Darkness
2=Pokemon XD: Equality Vesion
3=Pokemon XG: NeXt Gen
4=UNUSED
[Settings]
MaxChannels=4  # Maximum number of channels for this card
CardSize=64
```
---

!! ADDITIONAL !! : Files/Settings found in swiss SD
------------------------------------------------------------------------------------------------------------------------------------

| JP ID | JP Title | EN ID | EN Title |
|------|----------|-------|----------|
| GL3JE8 | ルパン三世：海に消えた秘宝 | GL3EE8 | Lupin III: Lost Treasure Under the Sea |

**SD Location:** `SD2SP2/SDGECKO/Swiss Location` 

`SD:/Swiss/settings/game/GL3EE8.ini`

```
ID=GL3EE8
Name=Lupin III (USA)
Comment=[Lupin Translation Team]
Status=Unknown
English Text Fix [Lupin Translation Team]
C20095B8 00000002
7CE0FA14 3A400000
60000000 00000000
C200A878 00000005
B003003A 3A4000FF
387D0000 38950000
3E208000 62318934
7E2903A6 4E800421
60000000 00000000
C200A88C 00000001
60000000 00000000
C200A860 00000007
B003003A 2C1200FF
41820014 3E208000
6231A87C 7E2903A6
4E800420 387D0000
38950000 3E208000
62318934 7E2903A6
4E800421 00000000
C2008968 00000001
60000000 00000000
```

---

| JP ID | JP Title | EN ID | EN Title |
|------|----------|-------|----------|
| GPZJ01 | NINTENDO パズルコレクション | GPZE01 | Nintendo Puzzle Collection |


`SD:/Swiss/settings/game/GPZE.ini`
```
# Game specific configuration file. Created by Swiss
ID=GPZE
Name=Nintendo Puzzle Collection
Comment=No Comment
Status=Unknown
```


## ❤️ Special Thanks
A huge thanks to [bbsan2k](https://github.com/bbsan2k) and [ManCloud](https://github.com/ManCloud) for creating such a fantastic piece of hardware!
