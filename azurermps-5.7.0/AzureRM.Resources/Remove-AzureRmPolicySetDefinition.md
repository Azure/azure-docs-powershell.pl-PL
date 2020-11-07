---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: fa96d686d66f9ef94322896974dc4dd3b81ad154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548003"
---
# <span data-ttu-id="44abb-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="44abb-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="44abb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44abb-102">SYNOPSIS</span></span>
<span data-ttu-id="44abb-103">Usuwa definicję zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="44abb-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44abb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44abb-104">SYNTAX</span></span>

### <span data-ttu-id="44abb-105">RemoveByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="44abb-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44abb-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="44abb-106">RemoveById</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44abb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="44abb-107">DESCRIPTION</span></span>
<span data-ttu-id="44abb-108">Polecenie cmdlet **Remove-AzureRmPolicySetDefinition** usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="44abb-108">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="44abb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44abb-109">EXAMPLES</span></span>

### <span data-ttu-id="44abb-110">Przykład 1: usuwanie definicji zestawu zasad według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="44abb-110">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="44abb-111">Pierwsze polecenie pobiera definicję zestawu zasad za pomocą polecenia cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="44abb-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="44abb-112">Polecenie zapisuje je w zmiennej $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="44abb-112">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="44abb-113">Drugie polecenie usuwa definicję zestawu zasad określoną przez właściwość **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="44abb-113">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="44abb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44abb-114">PARAMETERS</span></span>

### <span data-ttu-id="44abb-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="44abb-115">-ApiVersion</span></span>
<span data-ttu-id="44abb-116">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="44abb-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="44abb-117">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="44abb-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="44abb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44abb-118">-DefaultProfile</span></span>
<span data-ttu-id="44abb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="44abb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44abb-120">-Force</span><span class="sxs-lookup"><span data-stu-id="44abb-120">-Force</span></span>
<span data-ttu-id="44abb-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="44abb-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="44abb-122">-ID</span><span class="sxs-lookup"><span data-stu-id="44abb-122">-Id</span></span>
<span data-ttu-id="44abb-123">W pełni kwalifikowany identyfikator definicji zestawu zasad, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="44abb-123">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="44abb-124">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="44abb-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44abb-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44abb-125">-Name</span></span>
<span data-ttu-id="44abb-126">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="44abb-126">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44abb-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="44abb-127">-Pre</span></span>
<span data-ttu-id="44abb-128">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="44abb-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="44abb-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44abb-129">-Confirm</span></span>
<span data-ttu-id="44abb-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44abb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44abb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44abb-131">-WhatIf</span></span>
<span data-ttu-id="44abb-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44abb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44abb-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="44abb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44abb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44abb-134">CommonParameters</span></span>
<span data-ttu-id="44abb-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44abb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44abb-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44abb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44abb-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44abb-137">INPUTS</span></span>

### <span data-ttu-id="44abb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="44abb-138">System.String</span></span>

## <span data-ttu-id="44abb-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44abb-139">OUTPUTS</span></span>

### <span data-ttu-id="44abb-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44abb-140">System.Boolean</span></span>

## <span data-ttu-id="44abb-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44abb-141">NOTES</span></span>

## <span data-ttu-id="44abb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44abb-142">RELATED LINKS</span></span>