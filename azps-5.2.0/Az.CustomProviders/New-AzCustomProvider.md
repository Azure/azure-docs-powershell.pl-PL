---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339649"
---
# New-AzCustomProvider

## STRESZCZENIe
Umożliwia utworzenie lub zaktualizowanie niestandardowego dostawcy zasobów.

## POLECENIA

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Opis
Umożliwia utworzenie lub zaktualizowanie niestandardowego dostawcy zasobów.

## Przykłady

### Przykład 1. Tworzenie dostawcy niestandardowego
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

Tworzenie niestandardowego dostawcy zasobów

### Przykład 2: Tworzenie niestandardowego dostawcy ze skojarzeniami
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

Utwórz dostawcę niestandardowego z trasą dla skojarzeń dostawców niestandardowych.

## PARAMETRÓW

### -Action
Lista akcji implementowanych przez dostawcę zasobów niestandardowych.
Aby skonstruować, zobacz sekcję notatki dla właściwości akcji i Utwórz tabelę skrótów.

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

### -AsJob
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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Name (nazwa)
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

### -Nowait
Wykonywanie polecenia asynchronicznie

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
Lista typów zasobów implementowanych przez niestandardowego dostawcę zasobów.
Aby skonstruować, zobacz sekcję notatki dla właściwości ResourceType i Utwórz tablicę skrótów.

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

### -Subskrypcji
Identyfikator subskrypcji platformy Azure.
Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).

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

### -Tag
Znaczniki zasobów

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
Lista funkcji sprawdzania poprawności, które mają być uruchamiane na żądaniach niestandardowych dostawców zasobów.
Aby skonstruować, zobacz sekcję notatki dla właściwości sprawdzania poprawności i Utwórz tablicę skrótów.

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

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. CustomProviders. models. Api20180901Preview. ICustomRpManifest

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


ACTION <ICustomRpActionRouteDefinition [] >: lista akcji, które implementuje dostawca zasobów niestandardowych.
  - `Endpoint <String>`: Identyfikator URI punktu końcowego definicji trasy, do którego dostawca zasobów jest żądaniem serwera proxy. Może to być w postaci płaskiego identyfikatora URI (na przykład ' https://testendpoint/ ') lub może określać trasę za pośrednictwem ścieżki (na przykład ' https://testendpoint/{requestPath} ').
  - `Name <String>`: Nazwa definicji trasy. To jest nazwa rozszerzenia ARM (na przykład "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")
  - `[RoutingType <ActionRouting?>]`: Typy routingu obsługiwane w przypadku żądań akcji.

ResourceType <ICustomRpResourceTypeRouteDefinition [] >: Lista typów zasobów implementowanych przez niestandardowego dostawcę zasobów.
  - `Endpoint <String>`: Identyfikator URI punktu końcowego definicji trasy, do którego dostawca zasobów jest żądaniem serwera proxy. Może to być w postaci płaskiego identyfikatora URI (na przykład ' https://testendpoint/ ') lub może określać trasę za pośrednictwem ścieżki (na przykład ' https://testendpoint/{requestPath} ').
  - `Name <String>`: Nazwa definicji trasy. To jest nazwa rozszerzenia ARM (na przykład "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")
  - `[RoutingType <ResourceTypeRouting?>]`: Typy routingu obsługiwane dla żądań zasobów.

VALIDATION <ICustomRpValidations [] >: Lista funkcji sprawdzania poprawności, które mają zostać uruchomione na żądaniach niestandardowych dostawców zasobów.
  - `Specification <String>`: Łącze do specyfikacji sprawdzania poprawności. Specyfikacja musi być hostowana w raw.githubusercontent.com.
  - `[ValidationType <ValidationType?>]`: Typ walidacji, który ma zostać uruchomiony dla pasującego żądania.

## LINKI POKREWNE

