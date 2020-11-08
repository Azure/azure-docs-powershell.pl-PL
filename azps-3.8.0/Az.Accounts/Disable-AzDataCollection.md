---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/30/2020
ms.locfileid: "94054046"
---
# Disable-AzDataCollection

## STRESZCZENIe
Zrezygnowano z gromadzenia danych w celu ulepszenia poleceń cmdlet programu PowerShell w usłudze Azure. Dane są zbierane domyślnie, o ile użytkownik wyraźnie nie zrezygnuje.

## POLECENIA

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis

`Disable-AzDataCollection`Polecenie cmdlet umożliwia rezygnację z zbierania danych. Program Azure PowerShell domyślnie automatycznie zbiera dane telemetryczne. Aby wyłączyć zbieranie danych, musisz wyraźnie zrezygnować. Firma Microsoft gromadzi zebrane dane w celu zidentyfikowania wzorców użytkowania, identyfikowania typowych problemów oraz usprawnienia środowiska usługi Azure PowerShell. Program Microsoft Azure PowerShell nie gromadzi danych prywatnych ani osobistych. Jeśli wcześniej wybrałeś opcję, uruchom `Enable-AzDataCollection` polecenie cmdlet, aby ponownie włączyć zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.

## Przykłady

### Przykład 1: wyłączanie zbierania danych dla bieżącego użytkownika

W poniższym przykładzie pokazano, jak wyłączyć zbieranie danych dla bieżącego użytkownika.

```powershell
Disable-AzDataCollection
```

## PARAMETRÓW

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

Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

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

To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### System. void

## INFORMACYJN

## LINKI POKREWNE

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
