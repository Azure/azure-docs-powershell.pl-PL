---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 719ca5b8b837523359f4d55209956f7c68c3c93f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992132"
---
# Set-AzSynapseSqlActiveDirectoryAdministrator

## SYNOPSIS
Rezerwuje administratora usługi Azure AD dla puli języka SQL Synapse Analytics.

## SKŁADNIA

### SetByNameParameterSet (Domyślne)
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByInputObjectParameterSet
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByResourceIdParameterSet
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Set-AzSynapseSqlActiveDirectoryAdministrator** inicjałuje administratora usługi Azure Active Directory (Azure AD) dla obszaru roboczego analizy Azure Synapse Analytics w bieżącej subskrypcji.
W jednej chwili możesz zapewniać usługę tylko jednego administratora.
Poniższe elementy członkowskie usługi Azure AD mogą być aprowizowane jako administrator obszaru roboczego analizy Synapse:
- Natywne członkowie usługi Azure AD 
- Federowani członkowie usługi Azure AD 
- Zaimportowani członkowie z innych identyfikatorów Azure, którzy są członkami natywnymi lub federtywnymi 
- Grupy usługi Azure AD utworzone jako grupy zabezpieczeń konta Microsoft, takie jak konta Outlook.com, Hotmail.com lub Live.com, nie są obsługiwane jako administratorzy.
Inne konta gości, na przykład konta w domenach Gmail.com lub Yahoo.com, nie są obsługiwane jako administratorzy.
Zalecamy inicjowanie obsługi dedykowanej grupy usługi Azure AD jako administrator.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

To polecenie iniekuje grupę administratorów usługi Azure AD o nazwie DBAs dla obszaru roboczego o nazwie ContosoWorkspace.

### Przykład 2
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

To polecenie iniekuje grupę administratorów usługi Azure AD o nazwie DBAs dla obszaru roboczego o nazwie ContosoWorkspace.
Dzięki temu można mieć pewność, że polecenie zakończy się powodzeniem, nawet jeśli nazwa wyświetlana grupy nie jest unikatowa.

## PARAMETERS

### — AsJob
Uruchamianie polecenia cmdlet w tle

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

### — DisplayName
Określa nazwę wyświetlaną użytkownika lub grupy, dla której mają być udzielane uprawnienia.
Ta nazwa wyświetlana musi istnieć w usłudze Active Directory skojarzonej z bieżącą subskrypcją.

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

### -InputObject
obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
Określa identyfikator obiektu użytkownika lub grupy w usłudze Azure Active Directory, dla którego mają być udzielane uprawnienia.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu obszaru roboczego programu Synapse.

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Nazwa obszaru roboczego aplikacji Synapse.

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
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

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo

## NOTATKI

## LINKI POKREWNE
