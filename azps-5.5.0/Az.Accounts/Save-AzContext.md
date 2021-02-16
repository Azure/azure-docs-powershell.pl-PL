---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176578"
---
# Save-AzContext

## SYNOPSIS
Zapisuje bieżące informacje o uwierzytelnieniu do użycia w innych sesjach programu PowerShell.

## SKŁADNIA

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie Save-AzContext umożliwia zapisanie bieżących informacji o uwierzytelnieniu do użycia w innych sesjach programu PowerShell.

## PRZYKŁADY

### Przykład 1. Zapisywanie kontekstu bieżącej sesji
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

W tym przykładzie kontekst platformy Azure bieżącej sesji jest zapisywany w dostarczonym pliku JSON.

### Przykład 2. Zapisywanie danego kontekstu
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

W tym przykładzie jest zapisywany kontekst platformy Azure, który jest przekazywany do polecenia cmdlet w dostarczonym pliku JSON.

## PARAMETERS

### -DefaultProfile
Poświadczenia, dzierżawy i subskrypcja używane do komunikacji z platformą Azure.

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

### — Wymuszanie
Zastępowanie danego pliku, jeśli istnieje

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

### — Ścieżka
Określa ścieżkę pliku, w którym mają być zapisywanie informacji uwierzytelnianych.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Profil
Określa kontekst platformy Azure, z którego będzie odczytywane to polecenie cmdlet.
Jeśli nie określisz kontekstu, to polecenie cmdlet będzie odczytywane z lokalnego kontekstu domyślnego.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile

## OUTPUTS

### Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile

## NOTATKI

## LINKI POKREWNE
