---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: ce2c4060d6471cc65c6b343e86c1e15b74ca5414
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999041"
---
# Enable-AzDataCollection

## SYNOPSIS
Umożliwia programowi Azure PowerShell zbieranie danych w celu poprawy środowiska użytkownika za pomocą poleceń cmdlet programu Azure PowerShell. Wykonanie tego polecenia cmdlet wybiera opcję zbierania danych dla bieżącego użytkownika na bieżącym komputerze. Domyślnie dane są zbierane, chyba że użytkownik jawnie zrezygnuje.

## SKŁADNIA

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS

Polecenie `Enable-AzDataCollection` cmdlet służy do zbierania danych. Program Azure PowerShell domyślnie automatycznie zbiera dane telemetryczne. Firma Microsoft agreguje zebrane dane w celu identyfikowania wzorców użycia, identyfikowania typowych problemów i ulepszania środowiska programu Azure PowerShell.
Program Microsoft Azure PowerShell nie zbiera żadnych prywatnych ani osobistych danych. Aby wyłączyć zbieranie danych, musisz jawnie zrezygnować z wykonywania `Disable-AzDataCollection` tej funkcji.

## PRZYKŁADY

### Przykład 1. Włączanie zbierania danych dla bieżącego użytkownika

W poniższym przykładzie pokazano, jak włączyć zbieranie danych dla bieżącego użytkownika.

```powershell
Enable-AzDataCollection
```

## PARAMETERS

### -DefaultProfile

Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### — Potwierdź

Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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

Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### System.Void

## NOTATKI

## LINKI POKREWNE

[Disable-AzDataCollection](./Disable-AzDataCollection.md)
