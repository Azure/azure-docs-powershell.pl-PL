---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181154"
---
# New-AzCustomProvider

## SYNOPSIS
Tworzy lub aktualizuje niestandardowego dostawcę zasobów.

## SKŁADNIA

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## OPIS
Tworzy lub aktualizuje niestandardowego dostawcę zasobów.

## PRZYKŁADY

### Przykład 1. Tworzenie dostawcy niestandardowego
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

Tworzenie niestandardowego dostawcy zasobów

### Przykład 2. Tworzenie dostawcy niestandardowego ze skojarzeniami
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

Utwórz dostawcę niestandardowego z trasą dla niestandardowych skojarzeń dostawców.

## PARAMETERS

### — akcja
Lista akcji implementnych przez dostawcę zasobów niestandardowych.
Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach AKCJI i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — AsJob
Uruchamianie polecenia jako zadania

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
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacja
Lokalizacja zasobu

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

### — Nazwa
Nazwa dostawcy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Uruchamianie polecenia asynchronicznie

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

### -ResourceGroupName
Nazwa grupy zasobów.

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

### -ResourceType
Lista typów zasobów zaimplementowanych przez niestandardowego dostawcę zasobów.
Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach RESOURCETYPE i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SubscriptionId
Identyfikator subskrypcji platformy Azure.
Jest to ciąg w formacie GUID (np. 000000000-0000-0000-0000-0000000000000)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### — Tag
Tagi zasobów

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Sprawdzanie poprawności
Lista sprawdzania poprawności, które mają być uruchamiane na żądaniach niestandardowego dostawcy zasobów.
Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach sprawdzania poprawności i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

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

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.cmdlet.CustomProviders.Models.Api20180901Preview.ICustomRpManifest

## NOTATKI

ALIASY

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


ACTION <ICustomRpActionRouteDefinition[]>: lista akcji implementowania przez dostawcę zasobów niestandardowych.
  - `Endpoint <String>`: URI punktu końcowego definicji trasy, do których dostawca zasobów niestandardowych będzie żądał serwera proxy. Może to być w postaci płaskiego URI (np. ' ') lub określić trasę za pomocą ścieżki https://testendpoint/ (np. ' https://testendpoint/{requestPath} ')
  - `Name <String>`: nazwa definicji trasy. Stanie się to nazwą rozszerzenia ARM (np. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')
  - `[RoutingType <ActionRouting?>]`: Typy routingu obsługiwane w żądaniach akcji.

RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: lista typów zasobów implementowania przez niestandardowego dostawcę zasobów.
  - `Endpoint <String>`: URI punktu końcowego definicji trasy, do których dostawca zasobów niestandardowych będzie żądał serwera proxy. Może to być w postaci płaskiego URI (np. ' ') lub określić trasę za pomocą ścieżki https://testendpoint/ (np. ' https://testendpoint/{requestPath} ')
  - `Name <String>`: nazwa definicji trasy. Stanie się to nazwą rozszerzenia ARM (np. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')
  - `[RoutingType <ResourceTypeRouting?>]`: Typy routingu obsługiwane dla żądań zasobów.

SPRAWDZANIE <ICustomRpValidations[]>: lista sprawdzania poprawności, które mają być uruchamiane na żądaniach niestandardowego dostawcy zasobów.
  - `Specification <String>`: Link do specyfikacji sprawdzania poprawności. Specyfikacja musi być hostowana w raw.githubusercontent.com.
  - `[ValidationType <ValidationType?>]`: typ sprawdzania poprawności, który ma być uruchamiany względem zgodnego żądania.

## LINKI POKREWNE

