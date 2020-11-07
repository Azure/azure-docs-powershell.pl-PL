---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: e339becd21be14d3587252b88dd8069b266b2408
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93896969"
---
# <span data-ttu-id="f1428-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f1428-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="f1428-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f1428-102">SYNOPSIS</span></span>
<span data-ttu-id="f1428-103">Aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="f1428-103">Updates a workspace.</span></span>

## <span data-ttu-id="f1428-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f1428-104">SYNTAX</span></span>

### <span data-ttu-id="f1428-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f1428-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1428-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="f1428-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1428-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f1428-107">DESCRIPTION</span></span>
<span data-ttu-id="f1428-108">Polecenie cmdlet **Set-AzOperationalInsightsWorkspace** umożliwia zmianę konfiguracji obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="f1428-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="f1428-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f1428-109">EXAMPLES</span></span>

### <span data-ttu-id="f1428-110">Przykład 1. Zmienianie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="f1428-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="f1428-111">To polecenie modyfikuje jednostkę SKU i znaczniki obszaru roboczego o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f1428-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="f1428-112">Przykład 2: aktualizowanie obszaru roboczego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="f1428-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="f1428-113">To polecenie używa polecenia cmdlet Get-AzOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie webworkspace, a następnie przekazywać go do polecenia cmdlet **Set-AzOperationalInsightsWorkspace** przy użyciu operatora potoku w celu skonfigurowania jednostki SKU jako Premium.</span><span class="sxs-lookup"><span data-stu-id="f1428-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="f1428-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1428-114">PARAMETERS</span></span>

### <span data-ttu-id="f1428-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1428-115">-DefaultProfile</span></span>
<span data-ttu-id="f1428-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f1428-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1428-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f1428-117">-Name</span></span>
<span data-ttu-id="f1428-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="f1428-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="f1428-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1428-119">-ResourceGroupName</span></span>
<span data-ttu-id="f1428-120">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f1428-120">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="f1428-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f1428-121">-RetentionInDays</span></span>
<span data-ttu-id="f1428-122">Dane obszaru roboczego zachowywane w ciągu dni.</span><span class="sxs-lookup"><span data-stu-id="f1428-122">The workspace data retention in days.</span></span> <span data-ttu-id="f1428-123">730 dni to maksimum dozwolone dla wszystkich pozostałych wersji SKU</span><span class="sxs-lookup"><span data-stu-id="f1428-123">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="f1428-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="f1428-124">-Sku</span></span>
<span data-ttu-id="f1428-125">Określa poziom usług obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="f1428-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="f1428-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="f1428-126">Valid values are:</span></span> 
- <span data-ttu-id="f1428-127">niezależnych</span><span class="sxs-lookup"><span data-stu-id="f1428-127">free</span></span>
- <span data-ttu-id="f1428-128">Standard</span><span class="sxs-lookup"><span data-stu-id="f1428-128">standard</span></span>
- <span data-ttu-id="f1428-129">ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="f1428-129">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1428-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="f1428-130">-Tag</span></span>
<span data-ttu-id="f1428-131">Znaczniki zasobów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="f1428-131">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="f1428-132">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="f1428-132">-Workspace</span></span>
<span data-ttu-id="f1428-133">Określa obszar roboczy do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f1428-133">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="f1428-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1428-134">CommonParameters</span></span>
<span data-ttu-id="f1428-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1428-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1428-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1428-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1428-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1428-137">INPUTS</span></span>

### <span data-ttu-id="f1428-138">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f1428-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f1428-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f1428-139">System.String</span></span>

### <span data-ttu-id="f1428-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f1428-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f1428-141">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f1428-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f1428-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f1428-142">OUTPUTS</span></span>

### <span data-ttu-id="f1428-143">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f1428-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="f1428-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f1428-144">NOTES</span></span>

## <span data-ttu-id="f1428-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1428-145">RELATED LINKS</span></span>

[<span data-ttu-id="f1428-146">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="f1428-146">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="f1428-147">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f1428-147">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


