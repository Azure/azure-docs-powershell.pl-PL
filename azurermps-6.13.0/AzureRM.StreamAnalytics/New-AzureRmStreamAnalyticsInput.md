---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 2cce01f444566a91a7bc3b4b2395e1d4e3dacddc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524253"
---
# New-AzureRmStreamAnalyticsInput

## STRESZCZENIe
Tworzy lub aktualizuje dane wejściowe zlecenia.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmStreamAnalyticsInput** tworzy wejście w ramach zadania Stream Analytics lub aktualizuje istniejące dane.
Nazwę danych wejściowych można określić w pliku JSON lub w wierszu polecenia.
Jeśli oba te pola są określone, nazwa w wierszu polecenia musi być zgodna z nazwą w pliku.
Jeśli określisz dane wejściowe, które już istnieją, i nie określisz parametru *Force* , polecenie cmdlet wyświetli pytanie o to, czy zamienić istniejące dane.
Jeśli określisz parametr *Force* i określisz istniejącą nazwę wejściową, dane wejściowe zostaną zastąpione bez potwierdzenia.

## Przykłady

### PRZYKŁAD 1. Tworzenie wsadu pracy z definicją z pliku
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

To polecenie tworzy dane wejściowe z pliku, Input.json.
Jeśli istniejące dane wejściowe o nazwie określonej w pliku definicji wejściowej są już zdefiniowane, polecenie cmdlet wyświetli pytanie o to, czy chcesz je zamienić.

### PRZYKŁAD 2: Tworzenie danych wejściowych zlecenia
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

To polecenie tworzy nowe dane wejściowe zadania o nazwie EntryStream.
Jeśli istniejące dane wejściowe o tej nazwie są już zdefiniowane, polecenie cmdlet zwróci pytanie o to, czy zamienić je.

### PRZYKŁAD 3: zamienianie wsadu pracy na definicję z pliku
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

To polecenie zamienia definicję istniejącego źródła danych o nazwie EntryStream na definicję z pliku bez potwierdzenia.

## PARAMETRÓW

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

### -File (plik)
Określa ścieżkę do pliku JSON zawierającego reprezentację JSON usługi Azure Stream Analytics do utworzenia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
Określa nazwę zadania usługi Azure Stream Analytics, w którym można utworzyć dane wejściowe funkcji Analiza strumienia Azure.

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

### -Name (nazwa)
Określa nazwę danych wejściowych funkcji Analiza strumienia Azure do utworzenia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, w której należy utworzyć dane wejściowe usługi Azure Streaming.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. StreamAnalytics. models. PSInput

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmStreamAnalyticsInput](./Get-AzureRmStreamAnalyticsInput.md)

[Remove-AzureRmStreamAnalyticsInput](./Remove-AzureRmStreamAnalyticsInput.md)

[Test — AzureRmStreamAnalyticsInput](./Test-AzureRmStreamAnalyticsInput.md)


