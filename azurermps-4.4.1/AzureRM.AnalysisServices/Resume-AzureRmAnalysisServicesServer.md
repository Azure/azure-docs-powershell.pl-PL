---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 99f8eaae633f984cdd522576a3f65bf894143bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525826"
---
# Resume-AzureRmAnalysisServicesServer

## STRESZCZENIe
Wznawia działanie wystąpienia serwera usług Analysis Services

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Resume-AzureRmAnalysisServicesServer wznawia działanie wystąpienia serwera usług Analysis Services

## Przykłady

### Przykład 1
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

To polecenie spowoduje wznowienie wstrzymanego serwera o nazwie TestServer w ramach testera zasobów.

## PARAMETRÓW

### -Name (nazwa)
Nazwa serwera usług Analysis Services

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

### -PassThru
Po pomyślnym zakończeniu operacji zwróci dane usuniętego serwera.

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

### -ResourceGroupName
Nazwa grupy zasobów platformy Azure, do której należy serwer

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje użytkownika o potwierdzenie, czy wykonać operację.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer

## INFORMACYJN
Alias: Resume-AzureAs

## LINKI POKREWNE

[Get-AzureRmAnalysisServicesServer](./Get-AzureRmAnalysisServicesServer.md)

[Suspend — AzureRmAnalysisServicesServer](./Suspend-AzureRmAnalysisServicesServer.md)
