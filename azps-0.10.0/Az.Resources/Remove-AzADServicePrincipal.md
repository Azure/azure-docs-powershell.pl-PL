---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: bd58a044db49cdd0cedf2872e97e64662a49372c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398227"
---
# Remove-AzADServicePrincipal

## SYNOPSIS
Usuwa podmiot zabezpieczeń usługi Azure Active Directory.

## SKŁADNIA

### ObjectIdParameterSet (domyślne)
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

## OPIS
Usuwa podmiot zabezpieczeń usługi Azure Active Directory.

## PRZYKŁADY

### Przykład 1. Usuwanie podmiotu zabezpieczeń usługi według identyfikatora obiektu

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

Usuwa podmiot zabezpieczeń usługi z identyfikatorem obiektu '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.

### Przykład 2. Usuwanie podmiotu zabezpieczeń usługi według identyfikatora aplikacji

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

Usuwa podmiot zabezpieczeń usługi z identyfikatorem aplikacji '9263469e-d328-4321-8646-3e3e75d20e76".

### Przykład 3. Usuwanie podmiotu zabezpieczeń usługi przez dodatek SPN

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

Usuwanie podmiotu zabezpieczeń usługi przy użyciu nazwy głównej usługi "MyServicePrincipal"

### Przykład 4. Usuwanie podmiotu zabezpieczeń usługi za pomocą funkcji piping

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

Pobiera podmiot zabezpieczeń usługi z identyfikatorem obiektu "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" i potoki, które są do polecenia cmdlet programu Remove-AzADServicePrincipal w celu usunięcia tego podmiotu zabezpieczeń usługi.

### Przykład 5. Usuwanie podmiotu zabezpieczeń usługi przez stosowanie rur

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

Pobiera aplikację z identyfikatorem aplikacji "9263469e-d328-4321-8646-3e3e75d20e76" i potokami, które są przekierowywowane do polecenia cmdlet programu Remove-AzADServicePrincipal w celu usunięcia podmiotu zabezpieczeń usługi skojarzonego z tą aplikacją.

## PARAMETERS

### -ApplicationId
Identyfikator aplikacji podmiotu zabezpieczeń usługi.

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

### -ApplicationObject
Obiekt aplikacji, którego podmiot zabezpieczeń usługi jest usuwany.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### — DisplayName
Nazwa wyświetlana podmiotu zabezpieczeń usługi.

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

### — Wymuszanie
Przełączanie w celu usunięcia podmiotu zabezpieczeń usługi bez potwierdzenia.

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

### -InputObject
Obiekt podmiotu zabezpieczeń usługi.

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
Identyfikator obiektu podmiotu zabezpieczeń usługi do usunięcia.

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
Jeśli jest to określone, zwraca usunięty podmiot zabezpieczeń usługi.

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
Nazwa podmiotu zabezpieczeń usługi.

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

### System.Guid

### System.String

### Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parametry: InputObject (ByValue)

### Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parametry: ApplicationObject (ByValue)

## OUTPUTS

### Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal

## NOTATKI
Słowa kluczowe: azure, Az, arm, resource, management, manager, resource, group, template, deployment

## LINKI POKREWNE

[New-AzadServicePrincipal](./New-AzADServicePrincipal.md)

[Get-AzadServicePrincipal](./Get-AzADServicePrincipal.md)


[Remove-AzadApplication](./Remove-AzADApplication.md)

[Remove-AzadAppCredential](./Remove-AzADAppCredential.md)
