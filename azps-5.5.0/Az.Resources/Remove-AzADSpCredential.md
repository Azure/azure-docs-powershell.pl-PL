---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: bcb33f87b85eb6ad5bce9ba812ebccb4d154e920
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186394"
---
# Remove-AzADSpCredential

## SYNOPSIS
Usuwa poświadczenia podmiotu zabezpieczeń usługi.

## SKŁADNIA

### ObjectIdWithKeyIdParameterSet (domyślne)
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithKeyIdParameterSet
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyIdParameterSet
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalObjectParameterSet
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
To Remove-AzADSpCredential cmdlet może służyć do usuwania klucza poświadczeń od podmiotu zabezpieczeń usługi w przypadku naruszenia zabezpieczeń lub w ramach wygasania klucza poświadczeń.
Podmiot zabezpieczeń usługi jest identyfikowany przez dostarczenie identyfikatora obiektu lub nazwy podmiotu zabezpieczeń usługi (SPN).
Poświadczenia do usunięcia są identyfikowane za pomocą identyfikatora klucza, jeśli pojedyncze poświadczenia mają zostać usunięte, lub przełącznik "Wszystkie" w celu usunięcia wszystkich poświadczeń skojarzonych z podmiotem zabezpieczeń usługi.

## PRZYKŁADY

### Przykład 1. Usuwanie określonego poświadczenia podmiotu zabezpieczeń usługi

```powershell
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

Usuwa poświadczenia o identyfikatorze klucza "9044423a-60a3-45ac-9ab1-09534157ebb" podmiotu zabezpieczeń usługi z identyfikatorem obiektu '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.

### Przykład 2. Usuwanie wszystkich poświadczeń podmiotu zabezpieczeń usługi

```powershell
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

Usuwa wszystkie poświadczenia podmiotu zabezpieczeń usługi za pomocą dodatku SPN " http://test123 ".

### Przykład 3. Usuwanie wszystkich poświadczeń podmiotu zabezpieczeń usługi za pomocą funkcji pipingu

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

Pobiera podmiot zabezpieczeń usługi z identyfikatorem obiektu "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" i potokami, które są do polecenia cmdlet usługi Remove-AzADSpCredential w celu usunięcia wszystkich poświadczeń tego podmiotu zabezpieczeń usługi.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### — DisplayName
Nazwa wyświetlana podmiotu zabezpieczeń usługi.

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Wymuszanie
Przełącz się, aby usunąć poświadczenia bez potwierdzenia.

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

### -KeyId
Określa klucz poświadczeń do usunięcia.
Identyfikatory klucza podmiotu zabezpieczeń usługi można uzyskać za pomocą Get-AzADSpCredential cmdlet.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Identyfikator obiektu podmiotu zabezpieczeń usługi, z których mają być usuwane poświadczenia.

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.

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

### -ServicePrincipalName
Nazwa (SPN) podmiotu zabezpieczeń usługi, z których mają być usuwane poświadczenia.

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalObject
Obiekt podmiotu zabezpieczeń usługi, z który mają być usuwane poświadczenia.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal

### System.Guid

## DANE WYJŚCIOWE

### System.Boolean

## NOTATKI

## LINKI POKREWNE

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[New-AzADSpCredential](./New-AzADSpCredential.md)

[Get-AzadServicePrincipal](./Get-AzADServicePrincipal.md)

