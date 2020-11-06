---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: 157e7a3ee0cc7ea4a80517bf98d17c05df8c7899
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527070"
---
# Set-AzureRmBatchApplication

## STRESZCZENIe
Aktualizuje ustawienia określonej aplikacji.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmBatchApplication** modyfikuje ustawienia określonej aplikacji Azure Batch.

## Przykłady

### Przykład 1: aktualizowanie aplikacji na koncie wsadowym
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

To polecenie zmienia, czy aplikacja Llitware na koncie ContosoBatch zezwala na aktualizacje.
Polecenie nie powoduje zmiany domyślnej wersji ani nazwy wyświetlanej aplikacji.

## PARAMETRÓW

### -AccountName
Określa nazwę konta wsadowego, dla którego to polecenie cmdlet modyfikuje aplikację.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AllowUpdates
Określa, czy pakiety wewnątrz aplikacji mogą być zastępowane przy użyciu tego samego ciągu wersji.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Identyfikator aplikacji
Określa identyfikator aplikacji.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -DefaultVersion
Określa, który pakiet ma być używany, jeśli klient zażąda aplikacji, ale nie określa wersji.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisplayName
Określa nazwę wyświetlaną dla aplikacji.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej konto wsadowe.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmBatchApplication](./Get-AzureRmBatchApplication.md)

[Get-AzureRmBatchApplicationPackage](./Get-AzureRmBatchApplicationPackage.md)

[Nowe — AzureRmBatchApplication](./New-AzureRmBatchApplication.md)

[Nowe — AzureRmBatchApplicationPackage](./New-AzureRmBatchApplicationPackage.md)

[Remove-AzureRmBatchApplication](./Remove-AzureRmBatchApplication.md)

[Remove-AzureRmBatchApplicationPackage](./Remove-AzureRmBatchApplicationPackage.md)


