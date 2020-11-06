---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 795882aa421037252ca920093f1df39b4e242fce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527570"
---
# Revoke-AzureRmHDInsightHttpServicesAccess

## STRESZCZENIe
Wyłącza dostęp HTTP do klastra.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Revoke-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **REVOKE-AzureRmHDInsightHttpServicesAccess** wyłącza dostęp HTTP do klastra usługi Azure HDInsight dla usług ODBC, Ambari, Oozie i webHCatalog sieci Web.

## Przykłady

### Przykład 1: wyłączenie dostępu HTTP do klastra
```
PS C:\>Revoke-AzureRmHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

To polecenie odwołuje dostęp HTTP do klastra o nazwie-hadoop_001.

## PARAMETRÓW

### -Nazwaklastraname
Określa nazwę klastra.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### Microsoft. Azure. Management. HDInsight. MODELES. HttpConnectivitySettings

## INFORMACYJN

## LINKI POKREWNE

[Grant-AzureRmHDInsightHttpServicesAccess](./Grant-AzureRmHDInsightHttpServicesAccess.md)


