---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190547"
---
# <span data-ttu-id="4df15-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="4df15-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="4df15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4df15-102">SYNOPSIS</span></span>
<span data-ttu-id="4df15-103">Tworzenie lub aktualizowanie zestawu danych referencyjnych w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="4df15-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="4df15-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4df15-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4df15-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4df15-105">DESCRIPTION</span></span>
<span data-ttu-id="4df15-106">Tworzenie lub aktualizowanie zestawu danych referencyjnych w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="4df15-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="4df15-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4df15-107">EXAMPLES</span></span>

### <span data-ttu-id="4df15-108">Przykład 1. Tworzenie zestawu danych odwoływać się do określonego środowiska</span><span class="sxs-lookup"><span data-stu-id="4df15-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="4df15-109">To polecenie tworzy zestaw danych referencyjnych dla określonego środowiska.</span><span class="sxs-lookup"><span data-stu-id="4df15-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="4df15-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4df15-110">PARAMETERS</span></span>

### <span data-ttu-id="4df15-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="4df15-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="4df15-112">Zachowanie porównywania kluczy zestawu danych referencyjnych można ustawić przy użyciu tej właściwości.</span><span class="sxs-lookup"><span data-stu-id="4df15-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="4df15-113">Domyślnie wartość to "Porządkowa" — co oznacza, że podczas łączenia danych referencyjnych ze zdarzeniami lub dodawania nowych danych referencyjnych zostanie przeprowadzone porównanie z kluczem z rozróżnianą wielkością liter.</span><span class="sxs-lookup"><span data-stu-id="4df15-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="4df15-114">Gdy zostanie ustawiona wartość "OrdinalIgnoreCase", zostanie użyte porównanie bez uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="4df15-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.DataStringComparisonBehavior
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df15-115">-DefaultProfile</span></span>
<span data-ttu-id="4df15-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4df15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4df15-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="4df15-117">-EnvironmentName</span></span>
<span data-ttu-id="4df15-118">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="4df15-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="4df15-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="4df15-119">-KeyProperty</span></span>
<span data-ttu-id="4df15-120">Lista właściwości kluczy dla zestawu danych odwoływać się.</span><span class="sxs-lookup"><span data-stu-id="4df15-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="4df15-121">Aby skonstruować, zobacz sekcję NOTATKI dla właściwości KEYPROPERTY i utwórz tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="4df15-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetKeyProperty[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df15-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4df15-122">-Location</span></span>
<span data-ttu-id="4df15-123">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="4df15-123">The location of the resource.</span></span>

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

### <span data-ttu-id="4df15-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4df15-124">-Name</span></span>
<span data-ttu-id="4df15-125">Nazwa zestawu danych odwołania.</span><span class="sxs-lookup"><span data-stu-id="4df15-125">Name of the reference data set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df15-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df15-126">-ResourceGroupName</span></span>
<span data-ttu-id="4df15-127">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="4df15-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="4df15-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4df15-128">-SubscriptionId</span></span>
<span data-ttu-id="4df15-129">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4df15-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="4df15-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="4df15-130">-Tag</span></span>
<span data-ttu-id="4df15-131">Pary klucz-wartość dodatkowych właściwości zasobu.</span><span class="sxs-lookup"><span data-stu-id="4df15-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="4df15-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4df15-132">-Confirm</span></span>
<span data-ttu-id="4df15-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4df15-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4df15-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4df15-134">-WhatIf</span></span>
<span data-ttu-id="4df15-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4df15-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4df15-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4df15-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4df15-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df15-137">CommonParameters</span></span>
<span data-ttu-id="4df15-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4df15-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df15-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4df15-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df15-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4df15-140">INPUTS</span></span>

## <span data-ttu-id="4df15-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4df15-141">OUTPUTS</span></span>

### <span data-ttu-id="4df15-142">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="4df15-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="4df15-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4df15-143">NOTES</span></span>

<span data-ttu-id="4df15-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4df15-144">ALIASES</span></span>

<span data-ttu-id="4df15-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4df15-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4df15-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4df15-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4df15-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4df15-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4df15-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: Lista właściwości klucza dla zestawu danych odwołania.</span><span class="sxs-lookup"><span data-stu-id="4df15-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="4df15-149">`[Name <String>]`: nazwa właściwości klucza.</span><span class="sxs-lookup"><span data-stu-id="4df15-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="4df15-150">`[Type <ReferenceDataKeyPropertyType?>]`: typ właściwości klucza.</span><span class="sxs-lookup"><span data-stu-id="4df15-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="4df15-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4df15-151">RELATED LINKS</span></span>

