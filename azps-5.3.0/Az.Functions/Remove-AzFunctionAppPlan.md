---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501017"
---
# Remove-AzFunctionAppPlan

## STRESZCZENIe
Usuwa plan aplikacji funkcji.

## POLECENIA

### ByName (domyślny)
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Opis
Usuwa plan aplikacji funkcji.

## Przykłady

### Przykład 1: Uzyskaj plan aplikacji funkcji według nazwy i usuń go.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

To polecenie pobiera plan aplikacji o nazwie i usuwa go.

### Przykład 2: usuwanie planu aplikacji funkcji według nazwy.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

To polecenie usuwa plan aplikacji funkcji według nazwy.

## PARAMETRÓW

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

### -Force
Wymusza usunięcie funkcji polecenia cmdlet z planu aplikacji bez monitowania o potwierdzenie.

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

### -Name (nazwa)
Nazwa aplikacji funkcji.

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

### -PassThru
Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.

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

### System. Boolean

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

