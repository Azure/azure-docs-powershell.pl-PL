---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371469"
---
# <span data-ttu-id="849ca-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="849ca-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="849ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="849ca-102">SYNOPSIS</span></span>
<span data-ttu-id="849ca-103">Tworzenie lub aktualizowanie zestawu danych źródłowych w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="849ca-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="849ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="849ca-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="849ca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="849ca-105">DESCRIPTION</span></span>
<span data-ttu-id="849ca-106">Tworzenie lub aktualizowanie zestawu danych źródłowych w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="849ca-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="849ca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="849ca-107">EXAMPLES</span></span>

### <span data-ttu-id="849ca-108">Przykład 1. Tworzenie zestawu danych referencyjnych dla określonego środowiska</span><span class="sxs-lookup"><span data-stu-id="849ca-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="849ca-109">To polecenie tworzy dane referencyjne dla określonego środowiska.</span><span class="sxs-lookup"><span data-stu-id="849ca-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="849ca-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="849ca-110">PARAMETERS</span></span>

### <span data-ttu-id="849ca-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="849ca-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="849ca-112">Zachowanie porównania klucza zestawu danych źródłowych można ustawić za pomocą tej właściwości.</span><span class="sxs-lookup"><span data-stu-id="849ca-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="849ca-113">Wartość domyślna to "Liczba porządkowa", co oznacza, że podczas dołączania do danych przy użyciu zdarzeń lub dodawania nowych danych referencyjnych zostanie przeprowadzone porównanie klucza z uwzględnieniem wielkości liter.</span><span class="sxs-lookup"><span data-stu-id="849ca-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="849ca-114">Gdy jest ustawiona wartość "OrdinalIgnoreCase", zostanie użyte porównanie uwzględniające wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="849ca-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

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

### <span data-ttu-id="849ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849ca-115">-DefaultProfile</span></span>
<span data-ttu-id="849ca-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="849ca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="849ca-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="849ca-117">-EnvironmentName</span></span>
<span data-ttu-id="849ca-118">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="849ca-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="849ca-119">-Właściwość</span><span class="sxs-lookup"><span data-stu-id="849ca-119">-KeyProperty</span></span>
<span data-ttu-id="849ca-120">Lista właściwości klucza zestawu danych źródłowych.</span><span class="sxs-lookup"><span data-stu-id="849ca-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="849ca-121">Aby skonstruować, zobacz sekcję notatki dla właściwości właściwości i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="849ca-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="849ca-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="849ca-122">-Location</span></span>
<span data-ttu-id="849ca-123">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="849ca-123">The location of the resource.</span></span>

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

### <span data-ttu-id="849ca-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="849ca-124">-Name</span></span>
<span data-ttu-id="849ca-125">Nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="849ca-125">Name of the reference data set.</span></span>

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

### <span data-ttu-id="849ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="849ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="849ca-127">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="849ca-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="849ca-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="849ca-128">-SubscriptionId</span></span>
<span data-ttu-id="849ca-129">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="849ca-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="849ca-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="849ca-130">-Tag</span></span>
<span data-ttu-id="849ca-131">Pary klucz-wartość dodatkowych właściwości zasobu.</span><span class="sxs-lookup"><span data-stu-id="849ca-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="849ca-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="849ca-132">-Confirm</span></span>
<span data-ttu-id="849ca-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="849ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="849ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="849ca-134">-WhatIf</span></span>
<span data-ttu-id="849ca-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="849ca-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="849ca-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="849ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="849ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849ca-137">CommonParameters</span></span>
<span data-ttu-id="849ca-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="849ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849ca-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="849ca-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849ca-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="849ca-140">INPUTS</span></span>

## <span data-ttu-id="849ca-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="849ca-141">OUTPUTS</span></span>

### <span data-ttu-id="849ca-142">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="849ca-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="849ca-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="849ca-143">NOTES</span></span>

<span data-ttu-id="849ca-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="849ca-144">ALIASES</span></span>

<span data-ttu-id="849ca-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="849ca-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="849ca-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="849ca-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="849ca-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="849ca-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="849ca-148">Właściwość Key <IReferenceDataSetKeyProperty [] >: Lista właściwości klucza zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="849ca-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="849ca-149">`[Name <String>]`: Nazwa właściwości klucza.</span><span class="sxs-lookup"><span data-stu-id="849ca-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="849ca-150">`[Type <ReferenceDataKeyPropertyType?>]`: Typ właściwości klucza.</span><span class="sxs-lookup"><span data-stu-id="849ca-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="849ca-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="849ca-151">RELATED LINKS</span></span>

