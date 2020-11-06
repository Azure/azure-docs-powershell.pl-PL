---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 8c884e69dd13b96925940f467633baf515d88eda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543551"
---
# <span data-ttu-id="348c9-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="348c9-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="348c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="348c9-102">SYNOPSIS</span></span>
<span data-ttu-id="348c9-103">Aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="348c9-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="348c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="348c9-104">SYNTAX</span></span>

### <span data-ttu-id="348c9-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="348c9-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="348c9-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="348c9-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="348c9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="348c9-107">DESCRIPTION</span></span>
<span data-ttu-id="348c9-108">Polecenie cmdlet **Set-AzureRmOperationalInsightsWorkspace** umożliwia zmianę konfiguracji obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="348c9-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="348c9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="348c9-109">EXAMPLES</span></span>

### <span data-ttu-id="348c9-110">Przykład 1. Zmienianie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="348c9-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="348c9-111">To polecenie modyfikuje jednostkę SKU i znaczniki obszaru roboczego o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="348c9-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="348c9-112">Przykład 2: aktualizowanie obszaru roboczego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="348c9-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="348c9-113">To polecenie używa polecenia cmdlet Get-AzureRmOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie webworkspace, a następnie przekazywać go do polecenia cmdlet **Set-AzureRmOperationalInsightsWorkspace** przy użyciu operatora potoku w celu skonfigurowania jednostki SKU jako Premium.</span><span class="sxs-lookup"><span data-stu-id="348c9-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="348c9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="348c9-114">PARAMETERS</span></span>

### <span data-ttu-id="348c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="348c9-115">-DefaultProfile</span></span>
<span data-ttu-id="348c9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="348c9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="348c9-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="348c9-117">-Name</span></span>
<span data-ttu-id="348c9-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="348c9-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="348c9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="348c9-119">-ResourceGroupName</span></span>
<span data-ttu-id="348c9-120">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="348c9-120">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="348c9-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="348c9-121">-RetentionInDays</span></span>
<span data-ttu-id="348c9-122">Dane obszaru roboczego zachowywane w ciągu dni.</span><span class="sxs-lookup"><span data-stu-id="348c9-122">The workspace data retention in days.</span></span> <span data-ttu-id="348c9-123">730 dni to maksimum dozwolone dla wszystkich pozostałych wersji SKU</span><span class="sxs-lookup"><span data-stu-id="348c9-123">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="348c9-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="348c9-124">-Sku</span></span>
<span data-ttu-id="348c9-125">Określa poziom usług obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="348c9-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="348c9-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="348c9-126">Valid values are:</span></span> 
- <span data-ttu-id="348c9-127">niezależnych</span><span class="sxs-lookup"><span data-stu-id="348c9-127">free</span></span>
- <span data-ttu-id="348c9-128">Standard</span><span class="sxs-lookup"><span data-stu-id="348c9-128">standard</span></span>
- <span data-ttu-id="348c9-129">ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="348c9-129">premium</span></span>

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

### <span data-ttu-id="348c9-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="348c9-130">-Tag</span></span>
<span data-ttu-id="348c9-131">Znaczniki zasobów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="348c9-131">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="348c9-132">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="348c9-132">-Workspace</span></span>
<span data-ttu-id="348c9-133">Określa obszar roboczy do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="348c9-133">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="348c9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="348c9-134">CommonParameters</span></span>
<span data-ttu-id="348c9-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="348c9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="348c9-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="348c9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="348c9-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="348c9-137">INPUTS</span></span>

### <span data-ttu-id="348c9-138">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="348c9-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="348c9-139">Parametry: przestrzeń robocza (ByValue)</span><span class="sxs-lookup"><span data-stu-id="348c9-139">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="348c9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="348c9-140">System.String</span></span>

### <span data-ttu-id="348c9-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="348c9-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="348c9-142">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="348c9-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="348c9-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="348c9-143">OUTPUTS</span></span>

### <span data-ttu-id="348c9-144">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="348c9-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="348c9-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="348c9-145">NOTES</span></span>

## <span data-ttu-id="348c9-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="348c9-146">RELATED LINKS</span></span>

[<span data-ttu-id="348c9-147">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="348c9-147">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="348c9-148">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="348c9-148">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


