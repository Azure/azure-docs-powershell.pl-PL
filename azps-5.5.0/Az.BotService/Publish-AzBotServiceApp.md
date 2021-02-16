---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 4ef38ab40f90024124f7d5f09f1a55c16520dd6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200843"
---
# Publish-AzBotServiceApp

## SYNOPSIS
Zwraca wartość botservice określoną w parametrach.

## SKŁADNIA

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## OPIS
Zwraca wartość botservice określoną w parametrach.

## PRZYKŁADY

### Przykład 1. Publikowanie usługi BotService na platformie Azure
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

Publikowanie usługi BotService na platformie Azure według kodu

## PARAMETERS

### -CodeDir
Ten parametr definiuje ścieżkę pliku ZIP

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Ten parametr definiuje nazwę bota.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

## OUTPUTS

## NOTATKI

ALIASY

## LINKI POKREWNE

