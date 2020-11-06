---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 16a27c7756a25c4b8e4270a0c363f8a04528d12c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524941"
---
# <span data-ttu-id="f4dd3-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f4dd3-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="f4dd3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="f4dd3-103">Modyfikowanie definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="f4dd3-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4dd3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4dd3-104">SYNTAX</span></span>

### <span data-ttu-id="f4dd3-105">SetByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f4dd3-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4dd3-106">SetById</span><span class="sxs-lookup"><span data-stu-id="f4dd3-106">SetById</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4dd3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f4dd3-107">DESCRIPTION</span></span>
<span data-ttu-id="f4dd3-108">Polecenie cmdlet **Set-AzureRmPolicySetDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-108">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="f4dd3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4dd3-109">EXAMPLES</span></span>

### <span data-ttu-id="f4dd3-110">Przykład 1: aktualizowanie opisu definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="f4dd3-110">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="f4dd3-111">Pierwsze polecenie pobiera definicję zestawu zasad za pomocą polecenia cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="f4dd3-112">Polecenie zapisuje ten obiekt w zmiennej $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-112">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="f4dd3-113">Drugie polecenie aktualizuje opis definicji zestawu zasad określonego przez właściwość **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-113">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="f4dd3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4dd3-114">PARAMETERS</span></span>

### <span data-ttu-id="f4dd3-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f4dd3-115">-ApiVersion</span></span>
<span data-ttu-id="f4dd3-116">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f4dd3-117">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4dd3-118">-DefaultProfile</span></span>
<span data-ttu-id="f4dd3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f4dd3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4dd3-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="f4dd3-120">-Description</span></span>
<span data-ttu-id="f4dd3-121">Opis definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-121">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd3-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f4dd3-122">-DisplayName</span></span>
<span data-ttu-id="f4dd3-123">Nazwa wyświetlana definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-123">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd3-124">-ID</span><span class="sxs-lookup"><span data-stu-id="f4dd3-124">-Id</span></span>
<span data-ttu-id="f4dd3-125">Identyfikator definicji zasad w pełni kwalifikowany, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-125">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="f4dd3-126">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="f4dd3-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd3-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f4dd3-127">-Name</span></span>
<span data-ttu-id="f4dd3-128">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-128">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd3-129">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4dd3-129">-PolicyDefinition</span></span>
<span data-ttu-id="f4dd3-130">Definicja zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-130">The policy set definition.</span></span> <span data-ttu-id="f4dd3-131">Może to być ścieżka do nazwy pliku zawierającej definicje zasad lub definicji zestawu zasad jako ciągu.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-131">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd3-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="f4dd3-132">-Pre</span></span>
<span data-ttu-id="f4dd3-133">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd3-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f4dd3-134">-Confirm</span></span>
<span data-ttu-id="f4dd3-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4dd3-136">-WhatIf</span></span>
<span data-ttu-id="f4dd3-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4dd3-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4dd3-139">CommonParameters</span></span>
<span data-ttu-id="f4dd3-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4dd3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4dd3-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4dd3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4dd3-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4dd3-142">INPUTS</span></span>

### <span data-ttu-id="f4dd3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f4dd3-143">System.String</span></span>

## <span data-ttu-id="f4dd3-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4dd3-144">OUTPUTS</span></span>

### <span data-ttu-id="f4dd3-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f4dd3-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f4dd3-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4dd3-146">NOTES</span></span>

## <span data-ttu-id="f4dd3-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4dd3-147">RELATED LINKS</span></span>
