---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 54af80b230c3cb031e8927a82ec3536cc1a81ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999083"
---
# Disable-AzDataCollection

## SYNOPSIS
Zrezygnowano z gromadzenia danych w celu ulepszania poleceń cmdlet programu Azure PowerShell. Domyślnie dane są zbierane, chyba że użytkownik jawnie zrezygnuje.

## SKŁADNIA

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS

Polecenie `Disable-AzDataCollection` cmdlet służy do rezygnacji z z gromadzenia danych. Program Azure PowerShell domyślnie automatycznie zbiera dane telemetryczne. Aby wyłączyć zbieranie danych, musisz jawnie zrezygnować. Firma Microsoft agreguje zebrane dane w celu identyfikowania wzorców użycia, identyfikowania typowych problemów i ulepszania środowiska programu Azure PowerShell. Program Microsoft Azure PowerShell nie zbiera żadnych prywatnych ani osobistych danych. Jeśli wcześniej zrezygnowałeś(-aś), uruchom polecenie cmdlet, aby ponownie włączyć zbieranie danych dla bieżącego użytkownika `Enable-AzDataCollection` na bieżącym komputerze.

## PRZYKŁADY

### Przykład 1. Wyłączanie zbierania danych dla bieżącego użytkownika

W poniższym przykładzie pokazano, jak wyłączyć zbieranie danych dla bieżącego użytkownika.

```powershell
Disable-AzDataCollection
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

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
