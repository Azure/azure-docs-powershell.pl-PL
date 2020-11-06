---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: a09dae99d7a2b6e08dd255cc19b859aec89808f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546083"
---
# <span data-ttu-id="c6642-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c6642-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="c6642-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6642-102">SYNOPSIS</span></span>
<span data-ttu-id="c6642-103">Modyfikowanie definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="c6642-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6642-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6642-104">SYNTAX</span></span>

### <span data-ttu-id="c6642-105">Zestaw parametrów Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="c6642-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="c6642-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="c6642-106">(Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6642-107">Zestaw parametrów identyfikatora definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="c6642-107">The policy set definition Id parameter set.</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6642-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c6642-108">DESCRIPTION</span></span>
<span data-ttu-id="c6642-109">Polecenie cmdlet **Set-AzureRmPolicySetDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="c6642-109">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="c6642-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6642-110">EXAMPLES</span></span>

### <span data-ttu-id="c6642-111">Przykład 1: aktualizowanie opisu definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="c6642-111">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="c6642-112">Pierwsze polecenie pobiera definicję zestawu zasad za pomocą polecenia cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="c6642-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="c6642-113">Polecenie zapisuje ten obiekt w zmiennej $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="c6642-113">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="c6642-114">Drugie polecenie aktualizuje opis definicji zestawu zasad określonego przez właściwość **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="c6642-114">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="c6642-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6642-115">PARAMETERS</span></span>

### <span data-ttu-id="c6642-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c6642-116">-ApiVersion</span></span>
<span data-ttu-id="c6642-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="c6642-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c6642-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="c6642-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c6642-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="c6642-119">-Description</span></span>
<span data-ttu-id="c6642-120">Opis definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="c6642-120">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6642-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c6642-121">-DisplayName</span></span>
<span data-ttu-id="c6642-122">Nazwa wyświetlana definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="c6642-122">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6642-123">-ID</span><span class="sxs-lookup"><span data-stu-id="c6642-123">-Id</span></span>
<span data-ttu-id="c6642-124">Identyfikator definicji zasad w pełni kwalifikowany, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="c6642-124">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="c6642-125">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="c6642-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6642-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c6642-126">-Name</span></span>
<span data-ttu-id="c6642-127">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="c6642-127">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6642-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c6642-128">-PolicyDefinition</span></span>
<span data-ttu-id="c6642-129">Definicja zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="c6642-129">The policy set definition.</span></span> <span data-ttu-id="c6642-130">Może to być ścieżka do nazwy pliku zawierającej definicje zasad lub definicji zestawu zasad jako ciągu.</span><span class="sxs-lookup"><span data-stu-id="c6642-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6642-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="c6642-131">-Pre</span></span>
<span data-ttu-id="c6642-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="c6642-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c6642-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c6642-133">-Confirm</span></span>
<span data-ttu-id="c6642-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6642-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6642-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6642-135">-DefaultProfile</span></span>
<span data-ttu-id="c6642-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6642-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6642-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6642-137">-WhatIf</span></span>
<span data-ttu-id="c6642-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6642-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6642-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c6642-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6642-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6642-140">CommonParameters</span></span>
<span data-ttu-id="c6642-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6642-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6642-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6642-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6642-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6642-143">INPUTS</span></span>

### <span data-ttu-id="c6642-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c6642-144">System.String</span></span>

## <span data-ttu-id="c6642-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6642-145">OUTPUTS</span></span>

### <span data-ttu-id="c6642-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c6642-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c6642-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6642-147">NOTES</span></span>

## <span data-ttu-id="c6642-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6642-148">RELATED LINKS</span></span>

