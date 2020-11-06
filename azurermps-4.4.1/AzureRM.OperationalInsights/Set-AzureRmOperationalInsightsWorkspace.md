---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: e24597d25fffdc1b516c5a18cf011f7222d288c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527350"
---
# <span data-ttu-id="31800-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="31800-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="31800-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31800-102">SYNOPSIS</span></span>
<span data-ttu-id="31800-103">Aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="31800-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31800-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31800-104">SYNTAX</span></span>

### <span data-ttu-id="31800-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="31800-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31800-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="31800-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tags] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31800-107">Opis</span><span class="sxs-lookup"><span data-stu-id="31800-107">DESCRIPTION</span></span>
<span data-ttu-id="31800-108">Polecenie cmdlet **Set-AzureRmOperationalInsightsWorkspace** umożliwia zmianę konfiguracji obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="31800-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="31800-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31800-109">EXAMPLES</span></span>

### <span data-ttu-id="31800-110">Przykład 1. Zmienianie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="31800-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="31800-111">To polecenie modyfikuje jednostkę SKU i znaczniki obszaru roboczego o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="31800-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="31800-112">Przykład 2: aktualizowanie obszaru roboczego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="31800-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="31800-113">To polecenie używa polecenia cmdlet Get-AzureRmOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie webworkspace, a następnie przekazywać go do polecenia cmdlet **Set-AzureRmOperationalInsightsWorkspace** przy użyciu operatora potoku w celu skonfigurowania jednostki SKU jako Premium.</span><span class="sxs-lookup"><span data-stu-id="31800-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="31800-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31800-114">PARAMETERS</span></span>

### <span data-ttu-id="31800-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="31800-115">-Name</span></span>
<span data-ttu-id="31800-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="31800-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="31800-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31800-117">-ResourceGroupName</span></span>
<span data-ttu-id="31800-118">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="31800-118">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="31800-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="31800-119">-Sku</span></span>
<span data-ttu-id="31800-120">Określa poziom usług obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="31800-120">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="31800-121">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="31800-121">Valid values are:</span></span> 

- <span data-ttu-id="31800-122">niezależnych</span><span class="sxs-lookup"><span data-stu-id="31800-122">free</span></span>
- <span data-ttu-id="31800-123">Standard</span><span class="sxs-lookup"><span data-stu-id="31800-123">standard</span></span>
- <span data-ttu-id="31800-124">ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="31800-124">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: free, standard, premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31800-125">-Tagi</span><span class="sxs-lookup"><span data-stu-id="31800-125">-Tags</span></span>
<span data-ttu-id="31800-126">Określa znaczniki zasobów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="31800-126">Specifies the resource tags for the workspace.</span></span>

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

### <span data-ttu-id="31800-127">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="31800-127">-Workspace</span></span>
<span data-ttu-id="31800-128">Określa obszar roboczy do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="31800-128">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="31800-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31800-129">-DefaultProfile</span></span>
<span data-ttu-id="31800-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31800-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31800-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="31800-131">-RetentionInDays</span></span>
<span data-ttu-id="31800-132">Dane obszaru roboczego zachowywane w ciągu dni.</span><span class="sxs-lookup"><span data-stu-id="31800-132">The workspace data retention in days.</span></span> <span data-ttu-id="31800-133">730 dni to maksimum dozwolone dla wszystkich pozostałych wersji SKU.</span><span class="sxs-lookup"><span data-stu-id="31800-133">730 days is the maximum allowed for all other Skus.</span></span>

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

### <span data-ttu-id="31800-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31800-134">CommonParameters</span></span>
<span data-ttu-id="31800-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31800-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31800-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31800-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31800-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31800-137">INPUTS</span></span>

### <span data-ttu-id="31800-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="31800-138">PSWorkspace</span></span>
<span data-ttu-id="31800-139">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="31800-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="31800-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31800-140">OUTPUTS</span></span>

### <span data-ttu-id="31800-141">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="31800-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="31800-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31800-142">NOTES</span></span>

## <span data-ttu-id="31800-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31800-143">RELATED LINKS</span></span>

[<span data-ttu-id="31800-144">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="31800-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="31800-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="31800-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


