---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: a4584e4c0fc64920fbffb7e3d685a9be3ac04ad1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544240"
---
# <span data-ttu-id="ccafa-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ccafa-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="ccafa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ccafa-102">SYNOPSIS</span></span>
<span data-ttu-id="ccafa-103">Aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="ccafa-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccafa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ccafa-104">SYNTAX</span></span>

### <span data-ttu-id="ccafa-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ccafa-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ccafa-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="ccafa-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccafa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ccafa-107">DESCRIPTION</span></span>
<span data-ttu-id="ccafa-108">Polecenie cmdlet **Set-AzureRmOperationalInsightsWorkspace** umożliwia zmianę konfiguracji obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="ccafa-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="ccafa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ccafa-109">EXAMPLES</span></span>

### <span data-ttu-id="ccafa-110">Przykład 1. Zmienianie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="ccafa-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="ccafa-111">To polecenie modyfikuje jednostkę SKU i znaczniki obszaru roboczego o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ccafa-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="ccafa-112">Przykład 2: aktualizowanie obszaru roboczego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="ccafa-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="ccafa-113">To polecenie używa polecenia cmdlet Get-AzureRmOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie webworkspace, a następnie przekazywać go do polecenia cmdlet **Set-AzureRmOperationalInsightsWorkspace** przy użyciu operatora potoku w celu skonfigurowania jednostki SKU jako Premium.</span><span class="sxs-lookup"><span data-stu-id="ccafa-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="ccafa-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ccafa-114">PARAMETERS</span></span>

### <span data-ttu-id="ccafa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccafa-115">-DefaultProfile</span></span>
<span data-ttu-id="ccafa-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ccafa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccafa-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ccafa-117">-Name</span></span>
<span data-ttu-id="ccafa-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="ccafa-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccafa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccafa-119">-ResourceGroupName</span></span>
<span data-ttu-id="ccafa-120">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ccafa-120">Specifies the Azure resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccafa-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ccafa-121">-RetentionInDays</span></span>
<span data-ttu-id="ccafa-122">Dane obszaru roboczego zachowywane w ciągu dni.</span><span class="sxs-lookup"><span data-stu-id="ccafa-122">The workspace data retention in days.</span></span> <span data-ttu-id="ccafa-123">730 dni to maksimum dozwolone dla wszystkich pozostałych wersji SKU</span><span class="sxs-lookup"><span data-stu-id="ccafa-123">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccafa-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="ccafa-124">-Sku</span></span>
<span data-ttu-id="ccafa-125">Określa poziom usług obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="ccafa-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="ccafa-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="ccafa-126">Valid values are:</span></span> 

- <span data-ttu-id="ccafa-127">niezależnych</span><span class="sxs-lookup"><span data-stu-id="ccafa-127">free</span></span>
- <span data-ttu-id="ccafa-128">Standard</span><span class="sxs-lookup"><span data-stu-id="ccafa-128">standard</span></span>
- <span data-ttu-id="ccafa-129">ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="ccafa-129">premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccafa-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="ccafa-130">-Tag</span></span>
<span data-ttu-id="ccafa-131">Znaczniki zasobów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="ccafa-131">The resource tags for the workspace.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccafa-132">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="ccafa-132">-Workspace</span></span>
<span data-ttu-id="ccafa-133">Określa obszar roboczy do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="ccafa-133">Specifies the workspace to be updated.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccafa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccafa-134">CommonParameters</span></span>
<span data-ttu-id="ccafa-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccafa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccafa-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccafa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccafa-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccafa-137">INPUTS</span></span>

### <span data-ttu-id="ccafa-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ccafa-138">PSWorkspace</span></span>
<span data-ttu-id="ccafa-139">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="ccafa-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="ccafa-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ccafa-140">OUTPUTS</span></span>

### <span data-ttu-id="ccafa-141">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ccafa-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="ccafa-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ccafa-142">NOTES</span></span>

## <span data-ttu-id="ccafa-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ccafa-143">RELATED LINKS</span></span>

[<span data-ttu-id="ccafa-144">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="ccafa-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="ccafa-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ccafa-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


