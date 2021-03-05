---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: 522de6721d92b76938843b28322b94b5cc6ce481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963041"
---
# Update-AzFunctionAppPlan

## SYNOPSIS
Aktualizuje plan usługi aplikacji funkcyjnej.

## SKŁADNIA

### ByName (Default)
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## OPIS
Aktualizuje plan usługi aplikacji funkcyjnej.

## PRZYKŁADY

### Przykład 1. Aktualizowanie planu usługi aplikacji do wersji SKU EP2 z dwudziestoma maksymalnymi pracownikami.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

To polecenie aktualizuje plan usługi aplikacji do sKU EP2 z dwudziestoma maksymalnymi pracownikami.

## PARAMETERS

### — AsJob
Uruchom polecenie jako zadanie.

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

### -InputObject
Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumWorkerCount
Maksymalna liczba pracowników w planie usług aplikacji.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumLiczbowePracownika
Minimalna liczba pracowników w planie usług aplikacji.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Nazwa planu usługi aplikacji.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Uruchom polecenie asynchronicznie.

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
Nazwa grupy zasobów, do której należy zasób.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SKU
SKU planu.
Prawidłowe dane wejściowe: EP1, EP2, EP3

```yaml
Type: System.String
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

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### — Tag
Tagi zasobów.

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

### Microsoft.Azure.PowerShell.Cmdlet.Functions.Models.Api20190801.IAppServicePlan

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.Functions.Models.Api20190801.IAppServicePlan

## NOTATKI

ALIASY

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <IAppServicePlan> 
  - `Location <String>`: Lokalizacja zasobu.
  - `[Kind <String>]`: Rodzaj zasobu.
  - `[Tag <IResourceTags>]`: tagi zasobów.
    - `[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.
  - `[Capacity <Int32?>]`: Bieżąca liczba wystąpień przydzielonych do zasobu.
  - `[FreeOfferExpirationTime <DateTime?>]`: czas wygaśnięcia oferty bezpłatnej farmy serwerów.
  - `[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu w środowisku usługi aplikacji.
  - `[HyperV <Boolean?>]`: Jeśli plan usługi aplikacji kontenerowych Hyper-V — w <code>true</code> <code>false</code> przeciwnym razie.
  - `[IsSpot <Boolean?>]`: Jeśli <code>true</code> ten plan usług aplikacji jest właścicielem wystąpień spotowych.
  - `[IsXenon <Boolean?>]`: Przestarzałe: Jeśli plan usługi aplikacji kontenerowych Hyper-V <code>true</code> — <code>false</code> w przeciwnym razie.
  - `[MaximumElasticWorkerCount <Int32?>]`: Maksymalna liczba pracowników dozwolonych w tym planie usługi aplikacjiScaleEnabled
  - `[PerSiteScaling <Boolean?>]`: Jeśli aplikacje przypisane do tego planu usługi aplikacji <code>true</code> mogą być skalowane niezależnie.         Jeśli <code>false</code> aplikacje przypisane do tego planu usługi aplikacji zostaną przeskalowane do wszystkich wystąpień planu.
  - `[Reserved <Boolean?>]`: Jeśli plan usługi aplikacji dla systemu Linux <code>true</code> , <code>false</code> w przeciwnym razie.
  - `[SkuCapability <ICapability[]>]`: Czy włączono możliwości sKU, np. czy włączono Menedżera ruchu?
    - `[Name <String>]`: nazwa funkcji SKU.
    - `[Reason <String>]`: Przyczyna możliwości SKU.
    - `[Value <String>]`Wartość funkcji SKU.
  - `[SkuCapacityDefault <Int32?>]`: Domyślna liczba pracowników dla tego planu usługi aplikacji.
  - `[SkuCapacityMaximum <Int32?>]`: Maksymalna liczba pracowników dla tego planu usługi aplikacji.
  - `[SkuCapacityMinimum <Int32?>]`: Minimalna liczba pracowników dla tego planu usługi aplikacji.
  - `[SkuCapacityScaleType <String>]`: Dostępne konfiguracje skali dla planu usługi aplikacji.
  - `[SkuFamily <String>]`: Kod rodziny sku zasobu.
  - `[SkuLocation <String[]>]`: lokalizacje sku.
  - `[SkuName <String>]`: nazwa sku zasobu.
  - `[SkuSize <String>]`: Specyfikator rozmiaru sku zasobu.
  - `[SkuTier <String>]`: Warstwa usługi sku zasobu.
  - `[SpotExpirationTime <DateTime?>]`: czas wygaśnięcia farmy serwerów. Prawidłowy tylko w przypadku, gdy jest to farma serwerów spotowych.
  - `[TargetWorkerCount <Int32?>]`: skalowanie liczby pracowników.
  - `[TargetWorkerSizeId <Int32?>]`: skalowanie identyfikatora rozmiaru pracownika.
  - `[WorkerTierName <String>]`: Warstwa docelowa pracownika przypisana do planu usługi aplikacji.

## LINKI POKREWNE

