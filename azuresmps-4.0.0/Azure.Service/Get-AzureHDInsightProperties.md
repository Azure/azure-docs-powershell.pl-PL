---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 325DE85D-B9CB-4584-8C61-DA417736ABBF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55992408c1376c9456157387456b114c292b44c2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055317"
---
# Get-AzureHDInsightProperties

## STRESZCZENIe
Pobiera właściwości specyficzne dla usługi HDInsight.

## POLECENIA

```
Get-AzureHDInsightProperties [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Locations] [-Subscription <String>] [-Versions] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.
Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.
Użyj nowszej wersji usługi HDInsight Azure PowerShell.

Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Polecenie cmdlet **Get-AzureHDInsightProperties** pobiera właściwości specyficzne dla usługi Azure HDInsight, takiej jak lista dostępnych regionów platformy Azure, wersje klastra usługi HDInsight i dostępna pojemność obliczeniowa.

## Przykłady

### Przykład 1: uzyskiwanie właściwości usługi HDInsight dla subskrypcji
```
PS C:\>$SubName = Get-AzureSubscription -Current | %{ $_.SubscriptionName }
PS C:\> Get-AzureHDInsightProperties -Subscription $SubName
```

Pierwsze polecenie uzyskuje nazwę bieżącej subskrypcji platformy Azure, a następnie zapisuje ją w zmiennej $SubName.

Drugie polecenie pobiera właściwości usługi HDInsight dla subskrypcji w $SubName.

## PARAMETRÓW

### -Certificate
Określa certyfikat zarządzania dla subskrypcji platformy Azure.

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpoint
Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.
Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostedService
Określa obszar nazw usługi HDInsight.
Jeśli nie podano tego parametru, to polecenie cmdlet użyje domyślnego obszaru nazw.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreSslErrors
Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacje
Wskazuje, że ten aplet polecenia pobiera listę regionów platformy Azure, w których jest dostępna Usługa HDInsight.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subscription
Określa subskrypcję zawierającą właściwości usługi HDInsight do pobrania.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wersje
Wskazuje, że ten aplet polecenia pobiera listę wersji klastra usługi HDInsight, które są dostępne w usłudze dla subskrypcji.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

