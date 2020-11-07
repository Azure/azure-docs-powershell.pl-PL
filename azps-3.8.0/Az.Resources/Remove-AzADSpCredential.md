---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: 669a1beecaed14c0ab0705979188995daaf9d95f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895002"
---
# Remove-AzADSpCredential

## STRESZCZENIe
Usuwa poświadczenia z podmiotu zabezpieczeń usługi.

## POLECENIA

### ObjectIdWithKeyIdParameterSet (domyślny)
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

## Opis
Polecenia cmdlet Remove-AzADSpCredential można użyć w celu usunięcia klucza poświadczeń z podmiotu zabezpieczeń usługi w przypadku złamania zabezpieczeń lub jako część wygaśnięcia przerzucania klucza poświadczeń.
Wartość główna usługi jest identyfikowana przez podanie identyfikatora obiektu lub głównej nazwy usługi (SPN).
Poświadczenie, które ma zostać usunięte, jest identyfikowane przez identyfikator klucza, jeśli pojedyncze poświadczenie ma zostać usunięte lub z przełącznikiem wszystkie, aby usunąć wszystkie poświadczenia skojarzone z podmiotem zabezpieczeń usługi.

## Przykłady

### Przykład 1-Usuwanie konkretnego poświadczenia z podmiotu zabezpieczeń usługi

```
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

Usuwa poświadczenie o identyfikatorze klucza "9044423a-60a3-45ac-9ab1-09534157ebb" z podmiotu zabezpieczeń usługi z identyfikatorem obiektu "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82".

### Przykład 2 — Usuwanie wszystkich poświadczeń z podmiotu zabezpieczeń usługi

```
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

Usuwa wszystkie poświadczenia podmiotu zabezpieczeń usługi z główną nazwę użytkownika " http://test123 ".

### Przykład 3-Usuwanie wszystkich poświadczeń z podmiotu zabezpieczeń usługi przy użyciu połączeń rurowych

```
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

Pobiera podmiot zabezpieczeń usługi o identyfikatorze obiektu "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82" i potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzADSpCredential, aby usunąć wszystkie poświadczenia tego podmiotu usługi.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -DisplayName
Nazwa wyświetlana podmiotu usługi.

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

### -Force
Przełączanie do usuwania poświadczenia bez potwierdzenia.

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
Określa klucz poświadczenia, który ma zostać usunięty.
Identyfikatory kluczy dla podmiotu usługi można uzyskać przy użyciu polecenia cmdlet Get-AzADSpCredential.

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
Identyfikator obiektu podmiotu usługi, z którego mają zostać usunięte poświadczenia.

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
Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.

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
Nazwa (SPN) podmiotu usługi, z którego mają zostać usunięte poświadczenia.

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

### -Serviceprincipalobject
Obiekt główny usługi, z którego mają zostać usunięte poświadczenia.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. pozycji. PSADServicePrincipal

### System. GUID

## WYSYŁA

### System. Boolean

## INFORMACYJN

## LINKI POKREWNE

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[Nowe — AzADSpCredential](./New-AzADSpCredential.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

