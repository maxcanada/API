# Scaling


## Amounts

Asset quantities and totals transmitted via the CoinFLEX API are encoded as integers with an implicit scale factor that depends on the particular asset type. Assets showing a 2 at the end (such as XBTJAN2) represent bi-monthly future assets (starting and ending mid-month).

| Asset Type | ID (Hex) | ID (Dec) | Scale Factor |  Atomic Unit |
|:----------:|---------:|---------:|-------------:|-------------:|
|     XBT    |   0xF800 |    63488 |        10000 |     Ƀ 0.0001 |
|     BCH    |   0xF808 |    63496 |        10000 |    ɃC 0.0001 |
|     USDC   |   0xFF02 |    65282 |         1000 |     $C 0.001 |
|     USDT   |   0xFF03 |    65283 |         1000 |     $T 0.001 |
|  XBTJAN    |   0xC800 |    51200 |        10000 |  JanɃ 0.0001 |
|  XBTJAN2   |   0xCB20 |    52000 |        10000 | JanɃ2 0.0001 |
|  USDTJAN   |   0xCAA8 |    51880 |         1000 |  Jan$T 0.001 |
|  USDTJAN2  |   0xCF1C |    53020 |         1000 | Jan$T2 0.001 |
|  USDCJAN   |   0xCA94 |    51860 |         1000 |  Jan$C 0.001 |
|  USDCJAN2  |   0xCF08 |    53000 |         1000 | Jan$C2 0.001 |
|   XBTFEB   |   0xC801 |    51201 |        10000 |  FebɃ 0.0001 |
|   XBTFEB2  |   0xCB21 |    52001 |        10000 | FebɃ2 0.0001 |
|   USDTFEB  |   0xCAA9 |    51881 |         1000 |  Feb$T 0.001 |
|  USDTFEB2  |   0xCF1D |    53021 |         1000 | Feb$T2 0.001 |
|   USDCFEB  |   0xCA95 |    51861 |         1000 |  Feb$C 0.001 |
|  USDCFEB2  |   0xCF09 |    53001 |         1000 | Feb$C2 0.001 |
|   XBTMAR   |   0xC802 |    51202 |        10000 |  MarɃ 0.0001 |
|   XBTMAR2  |   0xCB22 |    52002 |        10000 | MarɃ2 0.0001 |
|   USDTMAR  |   0xCAAA |    51882 |         1000 |  Mar$T 0.001 |
|  USDTMAR2  |   0xCF1E |    53022 |         1000 | Mar$T2 0.001 |
|   USDCMAR  |   0xCA96 |    51862 |         1000 |  Mar$C 0.001 |
|  USDCMAR2  |   0xCF0A |    53002 |         1000 | Mar$C2 0.001 |
|   XBTAPR   |   0xC803 |    51203 |        10000 |  AprɃ 0.0001 |
|   XBTAPR2  |   0xCB23 |    52003 |        10000 | AprɃ2 0.0001 |
|   USDTAPR  |   0xCAAB |    51883 |         1000 |  Apr$T 0.001 |
|  USDTAPR2  |   0xCF1F |    53023 |         1000 | Apr$T2 0.001 |
|   USDCAPR  |   0xCA97 |    51863 |         1000 |  Apr$C 0.001 |
|  USDCAPR2  |   0xCF0B |    53003 |         1000 | Apr$C2 0.001 |
|   XBTMAY   |   0xC804 |    51204 |        10000 |  MayɃ 0.0001 |
|   XBTMAY2  |   0xCB24 |    52004 |        10000 | MayɃ2 0.0001 |
|   USDTMAY  |   0xCAAC |    51884 |         1000 |  May$T 0.001 |
|  USDTMAY2  |   0xCF20 |    53024 |         1000 | May$T2 0.001 |
|   USDCMAY  |   0xCA98 |    51864 |         1000 |  May$C 0.001 |
|  USDCMAY2  |   0xCF0C |    53004 |         1000 | May$C2 0.001 |
|   XBTJUN   |   0xC805 |    51205 |        10000 |  JunɃ 0.0001 |
|   XBTJUN2  |   0xCB25 |    52005 |        10000 | JunɃ2 0.0001 |
|   USDTJUN  |   0xCAAD |    51885 |         1000 |  Jun$T 0.001 |
|  USDTJUN2  |   0xCF21 |    53025 |         1000 | Jun$T2 0.001 |
|   USDCJUN  |   0xCA99 |    51865 |         1000 |  Jun$C 0.001 |
|  USDCJUN2  |   0xCF0D |    53005 |         1000 | Jun$C2 0.001 |
|   XBTJUL   |   0xC806 |    51206 |        10000 |  JulɃ 0.0001 |
|   XBTJUL2  |   0xCB26 |    52006 |        10000 | JulɃ2 0.0001 |
|   USDTJUL  |   0xCAAE |    51886 |         1000 |  Jul$T 0.001 |
|  USDTJUL2  |   0xCF22 |    53026 |         1000 | Jul$T2 0.001 |
|   USDCJUL  |   0xCA9A |    51866 |         1000 |  Jul$C 0.001 |
|  USDCJUL2  |   0xCF0E |    53006 |         1000 | Jul$C2 0.001 |
|   XBTAUG   |   0xC807 |    51207 |        10000 |  AugɃ 0.0001 |
|   XBTAUG2  |   0xCB27 |    52007 |        10000 | AugɃ2 0.0001 |
|   USDTAUG  |   0xCAAF |    51887 |         1000 |  Aug$T 0.001 |
|  USDTAUG2  |   0xCF23 |    53027 |         1000 | Aug$T2 0.001 |
|   USDCAUG  |   0xCA9B |    51867 |         1000 |  Aug$C 0.001 |
|  USDCAUG2  |   0xCF0F |    53007 |         1000 | Aug$C2 0.001 |
|   XBTSEP   |   0xC808 |    51208 |        10000 |  SepɃ 0.0001 |
|   XBTSEP2  |   0xCB28 |    52008 |        10000 | SepɃ2 0.0001 |
|   USDTSEP  |   0xCAB0 |    51888 |         1000 |  Sep$T 0.001 |
|  USDTSEP2  |   0xCF24 |    53028 |         1000 | Sep$T2 0.001 |
|   USDCSEP  |   0xCA9C |    51868 |         1000 |  Sep$C 0.001 |
|  USDCSEP2  |   0xCF10 |    53008 |         1000 | Sep$C2 0.001 |
|   XBTOCT   |   0xC809 |    51209 |        10000 |  OctɃ 0.0001 |
|   XBTOCT2  |   0xCB29 |    52009 |        10000 | OctɃ2 0.0001 |
|   USDTOCT  |   0xCAB1 |    51889 |         1000 |  Oct$T 0.001 |
|  USDTOCT2  |   0xCF25 |    53029 |         1000 | Oct$T2 0.001 |
|   USDCOCT  |   0xCA9D |    51869 |         1000 |  Oct$C 0.001 |
|  USDCOCT2  |   0xCF11 |    53009 |         1000 | Oct$C2 0.001 |
|   XBTNOV   |   0xC80A |    51210 |        10000 |  NovɃ 0.0001 |
|   XBTNOV2  |   0xCB2A |    52010 |        10000 | NovɃ2 0.0001 |
|   USDTNOV  |   0xCAB2 |    51890 |         1000 |  Nov$T 0.001 |
|  USDTNOV2  |   0xCF26 |    53030 |         1000 | Nov$T2 0.001 |
|   USDCNOV  |   0xCA9E |    51870 |         1000 |  Nov$C 0.001 |
|  USDCNOV2  |   0xCF12 |    53010 |         1000 | Nov$C2 0.001 |
|   XBTDEC   |   0xC80B |    51211 |        10000 |  DecɃ 0.0001 |
|   XBTDEC2  |   0xCB2B |    52011 |        10000 | DecɃ2 0.0001 |
|   USDTDEC  |   0xCAB3 |    51891 |         1000 |  Dec$T 0.001 |
|  USDTDEC2  |   0xCF27 |    53031 |         1000 | Dec$T2 0.001 |
|   USDCDEC  |   0xCA9F |    51871 |         1000 |  Dec$C 0.001 |
|  USDCDEC2  |   0xCF13 |    53011 |         1000 | Dec$C2 0.001 |

### Examples

| Logical Amount | Integer Encoding |
|---------------:|-----------------:|
|       Ƀ12.3456 |           123456 |
|       £9876.54 |           987654 |
|           Ƀ1.5 |            15000 |
|            £20 |             2000 |


## Prices

Prices transmitted via the CoinFLEX API are encoded as integers with an implicit scale factor that depends on the particular asset pair.

|    Asset Pair     | Scale Factor |
|:-----------------:|-------------:|
|      XBT:USDT     |         1000 |
|      USDT:USDC    |         1000 |
|   XBTJAN:USDTJAN  |         1000 |
|  XBTJAN2:USDTJAN2 |         1000 |
|   USDTJAN:USDCJAN |         1000 |
| USDTJAN2:USDCJAN2 |         1000 |
|   XBTFEB:USDTFEB  |         1000 |
|  XBTFEB2:USDTFEB2 |         1000 |
|  USDTFEB:USDCFEB  |         1000 |
| USDTFEB2:USDCFEB2 |         1000 |
|   XBTMAR:USDTMAR  |         1000 |
|  XBTMAR2:USDTMAR2 |         1000 |
|  USDTMAR:USDCMAR  |         1000 |
| USDTMAR2:USDCMAR2 |         1000 |
|  XBTAPR:USDTAPR   |         1000 |
| XBTAPR2:USDTAPR2  |         1000 |
|  USDTAPR:USDCAPR  |         1000 |
| USDTAPR2:USDCAPR2 |         1000 |
|  XBTMAY:USDTMAY   |         1000 |
| XBTMAY2:USDTMAY2  |         1000 |
|  USDTMAY:USDCMAY  |         1000 |
| USDTMAY2:USDCMAY2 |         1000 |
|  XBTJUN:USDTJUN   |         1000 |
| XBTJUN2:USDTJUN2  |         1000 |
|  USDTJUN:USDCJUN  |         1000 |
| USDTJUN2:USDCJUN2 |         1000 |
|  XBTJUL:USDTJUL   |         1000 |
| XBTJUL2:USDTJUL2  |         1000 |
|  USDTJUL:USDCJUL  |         1000 |
| USDTJUL2:USDCJUL2 |         1000 |
|  XBTAUG:USDTAUG   |         1000 |
| XBTAUG2:USDTAUG2  |         1000 |
|  USDTAUG:USDCAUG  |         1000 |
| USDTAUG2:USDCAUG2 |         1000 |
|  XBTSEP:USDTSEP   |         1000 |
| XBTSEP2:USDTSEP2  |         1000 |
|  USDTSEP:USDCSEP .|         1000 |
| USDTSEP2:USDCSEP2 |         1000 |
|  XBTOCT:USDTOCT   |         1000 |
| XBTOCT2:USDTOCT2  |         1000 |
|  USDTOCT:USDCOCT  |         1000 |
| USDTOCT2:USDCOCT2 |         1000 |
|  XBTNOV:USDTNOV   |         1000 |
| XBTNOV2:USDTNOV2  |         1000 |
|  USDTNOV:USDCNOV  |         1000 |
| USDTNOV2:USDCNOV2 |         1000 |
|  XBTDEC:USDTDEC   |         1000 |
| XBTDEC2:USDTDEC2  |         1000 |
|  USDTDEC:USDCDEC  |         1000 |
| USDTDEC2:USDCDEC2 |         1000 |


### Examples

| Logical Price | Integer Encoding |
|--------------:|-----------------:|
|   £543.21/XBT |            54321 |
|     £1000/XBT |           100000 |

