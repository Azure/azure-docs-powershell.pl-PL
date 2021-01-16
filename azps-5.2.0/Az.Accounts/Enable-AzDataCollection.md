---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333214"
---
# Enable-AzDataCollection

## STRESZCZENIe
Umożliwia zbieranie danych w celu usprawnienia środowiska użytkownika za pomocą poleceń cmdlet środowiska Azure PowerShell. Wykonanie tego polecenia cmdlet umożliwia zbieranie danych dla bieżącego użytkownika na bieżącym komputerze. Dane są zbierane domyślnie, o ile użytkownik wyraźnie nie zrezygnuje.

## POLECENIA

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis

Za pomocą polecenia cmdlet można dołączać `Enable-AzDataCollection` do kolekcji danych. Program Azure PowerShell domyślnie automatycznie zbiera dane telemetryczne. Firma Microsoft gromadzi zebrane dane w celu zidentyfikowania wzorców użytkowania, identyfikowania typowych problemów oraz usprawnienia środowiska usługi Azure PowerShell.
Program Microsoft Azure PowerShell nie gromadzi danych prywatnych ani osobistych. Aby wyłączyć zbieranie danych, należy wyraźnie zrezygnować z wykonywania `Disable-AzDataCollection` .

## Przykłady

### Przykład 1: Włączanie zbierania danych dla bieżącego użytkownika

W poniższym przykładzie pokazano, jak włączyć zbieranie danych dla bieżącego użytkownika.

```powershell
Enable-AzDataCollection
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

[Disable-AzDataCollection](./Disable-AzDataCollection.md)
