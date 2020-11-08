---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051400"
---
# Remove-AzBatchApplicationPackage

## STRESZCZENIe
Usuwa rekord pakietu aplikacji i plik binarny.

## POLECENIA

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzBatchApplicationPackage** usuwa rekord pakietu aplikacji i plik binarny z konta usługi Azure Batch.

## Przykłady

### Przykład 1: Usuwanie pakietu aplikacji z konta partii
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

To polecenie usuwa wersję 1,0 aplikacji Przykładowa z konta ContosoBatchGroup.
Polecenie usunie zarówno rekord pakietu, jak i obiekt BLOB zawierający plik binarny pakietu.

## PARAMETRÓW

### -AccountName
Określa nazwę konta wsadowego, z którego to polecenie cmdlet usuwa pakiet aplikacji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationName
Określa nazwę aplikacji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationVersion
Określa wersję aplikacji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej konto wsadowe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### System. void

## INFORMACYJN

## LINKI POKREWNE

[Get-AzBatchApplication](./Get-AzBatchApplication.md)

[Get-AzBatchApplicationPackage](./Get-AzBatchApplicationPackage.md)

[Nowe — AzBatchApplication](./New-AzBatchApplication.md)

[Nowe — AzBatchApplicationPackage](./New-AzBatchApplicationPackage.md)

[Remove-AzBatchApplication](./Remove-AzBatchApplication.md)

[Set-AzBatchApplication](./Set-AzBatchApplication.md)


