Broadcom 7445용 RDK 2.0 빌드하기
============================

1.Prerequisites
---------------

  broadcom에서 제공한 SoC RDK 포함, Source를 빌드하기 위해서는 먼저 directory 구조를 맞추어 줘야 한다.
FTP에서 가져온 총 5개의 파일 중, 아래의 file을 build하고자 하는 독립 directory에 복사해 넣고, 압축을 푼다.

```
file1) comcast_rdk_broadcom_release_rdk2.0_b14.1_20140418_humax.tgz
```
```
#> mkdir brcm7445_SoC_RDK2.0
#> cp comcast_rdk_broadcom_release_rdk2.0_b14.1_20140418_humax.tgz brcm7445_SoC_RDK2.0
#> cd brcm7445_SoC_RDK2.0
#> tar xfz comcast_rdk_broadcom_release_rdk2.0_b14.1_20140418_humax.tgz
```

압축을 풀면, tar 파일이 나오고 이또한 untar한다. 그럼 brcm에서 맞추어놓은 directory 및 파일들이 구성된다. 여
기에 FTP에서 가져온 5개의 파일 중 아래 2개의 file을 broadcom directory에 복사해 넣는다.

```
file2) refsw_release_unified_20140324.src.tgz
file3) trellis_release_14.1_20140407.src.tgz
```

그 후, 아래의 file을 thirdparty/broadcom directory에 복사해 넣는다.

```
file4) trellis_release_14.1_20140407_miracast.tgz
```

2. build 준비하기

  위에서 제일 먼저 압축을 풀었던 file1)의 데릭토리에 build에 참고할 수 있는 broadcom에서 release한 문서가
있다(Comcast_RDK2.0-B14.1_Broadcom_release_notes_20140418.pdf). 문서 내에 보면 
brcm97445vms를 빌드하기 위한 환경 설정 및 command가 나온다. 이것을 참고하여 아래처럼 입력하도록 하자.

```
#> export PATH=/usr/local/bin:/bin:/usr/bin:/usr/sbin:/sbin:/usr/bin/X11:/usr/openwin/bin:.:~/bin
#> export MANPATH=${MANPATH:-}:/usr/local/man
#> export PATH=`pwd`/comcast/rdkbuildtools:$PATH
#> export BRCM_RDK_REFSW_PKG=14.1
#> export BRCM_RDK_USE_TRELLIS=n (문서에는 y로 되어 있으나, 우린 n로 한다.)
```

그 후, prepare.sh를 돌려 build에 필요한 파일들이 생성되도록 한다.

```
#> ./prepare_combined_rdk2.0_b14.1.sh
```

위처럼 script를 실행시키면 opensource를 download 하는 등의 prepare과정을 하게 된다. prepare 과정이 끝
나면, build시 발생하는 compile error를 막기 위해 특정 환경 변수를 하나 추가한다. 파일 2개를 수정해야 하는데, 
파일의 위치는 아래와 같다.


