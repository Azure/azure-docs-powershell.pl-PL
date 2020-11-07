---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 28b95833e9221e5ecaa05ab33a6e2518c7cca1a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719187"
---
# Set-AzureRmHDInsightPersistedScriptAction

## STRESZCZENIe
Ustawia poprzednio wykonaną akcję skryptu, która będzie akcją utrwalonego skryptu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmHDInsightPersistedScriptAction** ustawia uprzednio wykonaną akcję skryptu, która jest akcją utrwaloną na skrypcie.
Określona akcja skryptu musiała już powieść.
Akcja skryptu zostanie uruchomiona za każdym razem, gdy klaster usługi Azure HDInsight będzie skalowany.

## Przykłady

### Przykład 1: Konfigurowanie wcześniej poprawnego skryptu, który ma zostać utrwalony, lub uruchamiania w celu skalowania klastra
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

To polecenie umożliwia ustawienie trwałej akcji skryptu, która została wykonana wcześniej, jako akcji skryptu.

## PARAMETRÓW

### -Nazwaklastraname
Określa nazwę klastra.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptExecutionId
Określa identyfikator wykonywania akcji skryptu, który ma zostać podwyższony do utrwalonego.
Akcja skryptu musiała się powieść, aby można było ją promować.
Identyfikator wykonywania akcji skryptu można znaleźć przy użyciu polecenia Get-AzureRmHDInsightScriptActionHistory.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### System. void

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmHDInsightPersistedScriptAction](./Get-AzureRmHDInsightPersistedScriptAction.md)

[Remove-AzureRmHDInsightPersistedScriptAction](./Remove-AzureRmHDInsightPersistedScriptAction.md)


