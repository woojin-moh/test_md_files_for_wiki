Broadcom 7445�� RDK 2.0 �����ϱ�
============================

1.Prerequisites
---------------

  broadcom���� ������ SoC RDK ����, Source�� �����ϱ� ���ؼ��� ���� directory ������ ���߾� ���� �Ѵ�.
FTP���� ������ �� 5���� ���� ��, �Ʒ��� file�� build�ϰ��� �ϴ� ���� directory�� ������ �ְ�, ������ Ǭ��.

```
file1) comcast_rdk_broadcom_release_rdk2.0_b14.1_20140418_humax.tgz
```

```
#> mkdir brcm7445_SoC_RDK2.0
#> cp comcast_rdk_broadcom_release_rdk2.0_b14.1_20140418_humax.tgz brcm7445_SoC_RDK2.0
#> cd brcm7445_SoC_RDK2.0
#> tar xfz comcast_rdk_broadcom_release_rdk2.0_b14.1_20140418_humax.tgz
```

������ Ǯ��, tar ������ ������ �̶��� untar�Ѵ�. �׷� brcm���� ���߾����� directory �� ���ϵ��� �����ȴ�. ��
�⿡ FTP���� ������ 5���� ���� �� �Ʒ� 2���� file�� broadcom directory�� ������ �ִ´�.

```
file2) refsw_release_unified_20140324.src.tgz
file3) trellis_release_14.1_20140407.src.tgz
```

�� ��, �Ʒ��� file�� thirdparty/broadcom directory�� ������ �ִ´�.

```
file4) trellis_release_14.1_20140407_miracast.tgz
```

2. build �غ��ϱ�

  ������ ���� ���� ������ Ǯ���� file1)�� �����丮�� build�� ������ �� �ִ� broadcom���� release�� ������
�ִ�(Comcast_RDK2.0-B14.1_Broadcom_release_notes_20140418.pdf). ���� ���� ���� 
brcm97445vms�� �����ϱ� ���� ȯ�� ���� �� command�� ���´�. �̰��� �����Ͽ� �Ʒ�ó�� �Է��ϵ��� ����.

```
#> export PATH=/usr/local/bin:/bin:/usr/bin:/usr/sbin:/sbin:/usr/bin/X11:/usr/openwin/bin:.:~/bin
#> export MANPATH=${MANPATH:-}:/usr/local/man
#> export PATH=`pwd`/comcast/rdkbuildtools:$PATH
#> export BRCM_RDK_REFSW_PKG=14.1
#> export BRCM_RDK_USE_TRELLIS=n (�������� y�� �Ǿ� ������, �츰 n�� �Ѵ�.)
```

�� ��, prepare.sh�� ���� build�� �ʿ��� ���ϵ��� �����ǵ��� �Ѵ�.

```
#> ./prepare_combined_rdk2.0_b14.1.sh
```

��ó�� script�� ������Ű�� opensource�� download �ϴ� ���� prepare������ �ϰ� �ȴ�. prepare ������ ��
����, build�� �߻��ϴ� compile error�� ���� ���� Ư�� ȯ�� ������ �ϳ� �߰��Ѵ�. ���� 2���� �����ؾ� �ϴµ�, 
������ ��ġ�� �Ʒ��� ����.


