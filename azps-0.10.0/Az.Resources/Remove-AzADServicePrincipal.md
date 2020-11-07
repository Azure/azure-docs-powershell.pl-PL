---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 966b9baf35f1719f29fda6355a9675739693314f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892437"
---
# Remove-AzADServicePrincipal

## STRESZCZENIe
Usuwa podmiot zabezpieczeń usługi Azure Active Directory.

## POLECENIA

### ObjectIdParameterSet (domyślny)
```
Remove-AzADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNParameterSet
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectParameterSet
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectParameterSet
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Usuwa podmiot zabezpieczeń usługi Azure Active Directory.

## Przykłady

### Przykład 1 — Usuwanie podmiotu zabezpieczeń usługi według identyfikatora obiektu

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

Usuwa podmiot zabezpieczeń usługi z identyfikatorem obiektu "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45".

### Przykład 2 — Usuwanie podmiotu zabezpieczeń usługi według identyfikatora aplikacji

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

Usuwa podmiot zabezpieczeń usługi z identyfikatorem aplikacji "9263469e-d328-4321-8646-3e3e75d20e76".

### Przykład 3 — Usuwanie podmiotu zabezpieczeń usługi według nazwy SPN

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

Usuwanie podmiotu usługi z nazwą główną usługi "MyServicePrincipal"

### Przykład 4 — Usuwanie podmiotu zabezpieczeń usługi według połączeń rurowych

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

Pobiera podmiot zabezpieczeń usługi o identyfikatorze obiektu "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" i potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzADServicePrincipal w celu usunięcia tego podmiotu usługi.

### Przykład 5 — Usuwanie podmiotu usługi przez potok aplikacji

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

Pobiera aplikację o identyfikatorze aplikacji "9263469e-d328-4321-8646-3e3e75d20e76" i potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzADServicePrincipal w celu usunięcia podmiotu usługi skojarzonego z tą aplikacją.

## PARAMETRÓW

### -Identyfikator aplikacji
Identyfikator głównej aplikacji usługi.

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Applicationobject
Obiekt aplikacji, którego podmiot usługi jest usuwany.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

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
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Przełączanie do Usuń podmiot zabezpieczeń usługi bez potwierdzenia.

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

### -Inputobject
Główny obiekt usługi.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
Identyfikator obiektu podmiotu usługi, który ma zostać usunięty.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Jeśli ta funkcja jest określona, zwraca usunięty podmiot zabezpieczeń usługi.

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
Nazwa główna usługi.

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. GUID

### System. String

### Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal
Parametry: Inputobject (ByValue)

### Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication
Parametry: Applicationobject (ByValue)

## WYSYŁA

### Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal

## INFORMACYJN
Słowa kluczowe: Azure, AZ, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie

## LINKI POKREWNE

[Nowe — AzADServicePrincipal](./New-AzADServicePrincipal.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

[Set-AzADServicePrincipal](./Set-AzADServicePrincipal.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)

[Remove-AzADAppCredential](./Remove-AzADAppCredential.md)
