---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345250"
---
# Update-AzFunctionAppPlan

## STRESZCZENIe
Aktualizuje plan usługi App Service.

## POLECENIA

### ByName (domyślny)
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

## Opis
Aktualizuje plan usługi App Service.

## Przykłady

### Przykład 1: aktualizowanie planu usługi App Service, aby EP2 SKU z 20 maksymalnymi pracownikami.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

To polecenie aktualizuje plan usługi App Service, aby EP2 SKU z 20 maksymalnymi pracownikami.

## PARAMETRÓW

### -AsJob
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

### -Inputobject
Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.

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
Maksymalna liczba pracowników planu usługi App Service.

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

### -MinimumWorkerCount
Minimalna liczba pracowników planu usługi App Service.

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

### -Name (nazwa)
Nazwa planu usługi App Service.

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

### -Nowait
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

### -SKU
Wersja planu.
Prawidłowe dane wejściowe to: EP1, EP2, EP3

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

### -Subskrypcji
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

### -Tag
Znaczniki zasobów.

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

### Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. IAppServicePlan

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. IAppServicePlan

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


INPUTobject <IAppServicePlan> : 
  - `Location <String>`: Lokalizacja zasobu.
  - `[Kind <String>]`: Rodzaj zasobu.
  - `[Tag <IResourceTags>]`: Znaczniki zasobów.
    - `[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.
  - `[Capacity <Int32?>]`: Bieżąca liczba wystąpień przydzielonych do zasobu.
  - `[FreeOfferExpirationTime <DateTime?>]`: Czas wygaśnięcia bezpłatnej oferty farmy serwerów.
  - `[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu środowiska App Service Environment.
  - `[HyperV <Boolean?>]`: Jeśli plan usługi App Service kontener funkcji Hyper-V jest <code>true</code> <code>false</code> inny, w przeciwnym razie.
  - `[IsSpot <Boolean?>]`: Jeśli <code>true</code> ten plan usługi App Service jest właścicielem wystąpień dodatkowych.
  - `[IsXenon <Boolean?>]`: Przestarzałe: Jeśli plan usługi App Service kontener funkcji Hyper-V jest <code>true</code> <code>false</code> inny, w przeciwnym razie.
  - `[MaximumElasticWorkerCount <Int32?>]`: Maksymalna liczba wszystkich pracowników dozwolonych dla tego planu usługi App Service ElasticScaleEnabled
  - `[PerSiteScaling <Boolean?>]`: Jeśli <code>true</code> aplikacje przydzielone do tego planu usługi App Service mogą być skalowane niezależnie.         Jeśli <code>false</code> aplikacje przydzielone do tego planu usługi App Service będą skalowane do wszystkich wystąpień planu.
  - `[Reserved <Boolean?>]`: Jeśli plan usługi Linux App Service jest <code>true</code> <code>false</code> inny, w przeciwnym razie.
  - `[SkuCapability <ICapability[]>]`: Funkcje jednostki SKU, na przykład, są włączone w usłudze Traffic Manager?
    - `[Name <String>]`: Nazwa funkcji SKU.
    - `[Reason <String>]`: Przyczyna funkcji SKU.
    - `[Value <String>]`: Wartość funkcji SKU.
  - `[SkuCapacityDefault <Int32?>]`: Domyślna liczba pracowników tej jednostki SKU planu usługi App Service.
  - `[SkuCapacityMaximum <Int32?>]`: Maksymalna liczba pracowników tej jednostki SKU planu usługi App Service.
  - `[SkuCapacityMinimum <Int32?>]`: Minimalna liczba pracowników dla tej jednostki SKU planu usługi App Service.
  - `[SkuCapacityScaleType <String>]`: Dostępne konfiguracje skali dla planu usługi App Service.
  - `[SkuFamily <String>]`: Kod rodziny w wersji SKU zasobu.
  - `[SkuLocation <String[]>]`: Lokalizacje jednostki SKU.
  - `[SkuName <String>]`: Nazwa SKU zasobu.
  - `[SkuSize <String>]`: Określenie rozmiaru jednostki SKU zasobu.
  - `[SkuTier <String>]`: Warstwa usługi SKU zasobu.
  - `[SpotExpirationTime <DateTime?>]`: Czas wygaśnięcia farmy serwerów. Ważne tylko w przypadku, gdy jest to farma serwera dodatkowego.
  - `[TargetWorkerCount <Int32?>]`: Liczba przeskalowania pracownika.
  - `[TargetWorkerSizeId <Int32?>]`: Skalowanie rozmiaru pracownika.
  - `[WorkerTierName <String>]`: Warstwa docelowa roboczego przypisana do planu usługi App Service.

## LINKI POKREWNE

