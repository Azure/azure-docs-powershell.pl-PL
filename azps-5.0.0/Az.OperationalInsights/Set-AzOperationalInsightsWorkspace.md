---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 5abfd1a02687eb2715ad924510176748e04e56cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317898"
---
# <span data-ttu-id="9401c-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="9401c-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="9401c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9401c-102">SYNOPSIS</span></span>
<span data-ttu-id="9401c-103">Aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9401c-103">Updates a workspace.</span></span>

## <span data-ttu-id="9401c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9401c-104">SYNTAX</span></span>

### <span data-ttu-id="9401c-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9401c-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="9401c-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="9401c-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="9401c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9401c-107">DESCRIPTION</span></span>
<span data-ttu-id="9401c-108">Polecenie cmdlet **Set-AzOperationalInsightsWorkspace** umożliwia zmianę konfiguracji obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9401c-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="9401c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9401c-109">EXAMPLES</span></span>

### <span data-ttu-id="9401c-110">Przykład 1. Zmienianie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="9401c-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="9401c-111">To polecenie modyfikuje jednostkę SKU i znaczniki obszaru roboczego o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9401c-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="9401c-112">Przykład 2: aktualizowanie obszaru roboczego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="9401c-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="9401c-113">To polecenie używa polecenia cmdlet Get-AzOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie webworkspace, a następnie przekazywać go do polecenia cmdlet **Set-AzOperationalInsightsWorkspace** przy użyciu operatora potoku w celu skonfigurowania jednostki SKU jako Premium.</span><span class="sxs-lookup"><span data-stu-id="9401c-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="9401c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9401c-114">PARAMETERS</span></span>

### <span data-ttu-id="9401c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9401c-115">-DefaultProfile</span></span>
<span data-ttu-id="9401c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9401c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9401c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9401c-117">-Name</span></span>
<span data-ttu-id="9401c-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9401c-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9401c-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="9401c-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="9401c-120">Typ dostępu do sieci umożliwiający dostęp do spożycia w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="9401c-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="9401c-121">Wartość powinna być równa "Enabled" lub "Disabled"</span><span class="sxs-lookup"><span data-stu-id="9401c-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="9401c-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="9401c-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="9401c-123">Typ dostępu do sieci w celu uzyskania dostępu do zapytania dotyczącego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9401c-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="9401c-124">Wartość powinna być równa "Enabled" lub "Disabled"</span><span class="sxs-lookup"><span data-stu-id="9401c-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="9401c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9401c-125">-ResourceGroupName</span></span>
<span data-ttu-id="9401c-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9401c-126">Specifies the Azure resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9401c-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9401c-127">-RetentionInDays</span></span>
<span data-ttu-id="9401c-128">Dane obszaru roboczego zachowywane w ciągu dni.</span><span class="sxs-lookup"><span data-stu-id="9401c-128">The workspace data retention in days.</span></span> <span data-ttu-id="9401c-129">730 dni to maksimum dozwolone dla wszystkich pozostałych wersji SKU</span><span class="sxs-lookup"><span data-stu-id="9401c-129">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9401c-130">-SKU</span><span class="sxs-lookup"><span data-stu-id="9401c-130">-Sku</span></span>
<span data-ttu-id="9401c-131">Określa poziom usług obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9401c-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="9401c-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="9401c-132">Valid values are:</span></span> 
- <span data-ttu-id="9401c-133">niezależnych</span><span class="sxs-lookup"><span data-stu-id="9401c-133">free</span></span>
- <span data-ttu-id="9401c-134">Standard</span><span class="sxs-lookup"><span data-stu-id="9401c-134">standard</span></span>
- <span data-ttu-id="9401c-135">ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="9401c-135">premium</span></span>
- <span data-ttu-id="9401c-136">pernode</span><span class="sxs-lookup"><span data-stu-id="9401c-136">pernode</span></span>
- <span data-ttu-id="9401c-137">oddzielnie</span><span class="sxs-lookup"><span data-stu-id="9401c-137">standalone</span></span>
- <span data-ttu-id="9401c-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="9401c-138">pergb2018</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone, pergb2018

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9401c-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="9401c-139">-Tag</span></span>
<span data-ttu-id="9401c-140">Znaczniki zasobów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9401c-140">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9401c-141">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="9401c-141">-Workspace</span></span>
<span data-ttu-id="9401c-142">Określa obszar roboczy do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="9401c-142">Specifies the workspace to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9401c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9401c-143">CommonParameters</span></span>
<span data-ttu-id="9401c-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9401c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9401c-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9401c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9401c-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9401c-146">INPUTS</span></span>

### <span data-ttu-id="9401c-147">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9401c-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="9401c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9401c-148">System.String</span></span>

### <span data-ttu-id="9401c-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9401c-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9401c-150">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9401c-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9401c-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9401c-151">OUTPUTS</span></span>

### <span data-ttu-id="9401c-152">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9401c-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="9401c-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9401c-153">NOTES</span></span>

## <span data-ttu-id="9401c-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9401c-154">RELATED LINKS</span></span>

[<span data-ttu-id="9401c-155">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="9401c-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="9401c-156">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="9401c-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


