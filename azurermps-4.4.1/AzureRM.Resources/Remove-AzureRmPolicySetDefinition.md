---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d3b9d8af81f08786536abf0d26b3c4ba2f2d66bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717796"
---
# <span data-ttu-id="f64fb-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f64fb-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="f64fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f64fb-102">SYNOPSIS</span></span>
<span data-ttu-id="f64fb-103">Usuwa definicję zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f64fb-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f64fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f64fb-104">SYNTAX</span></span>

### <span data-ttu-id="f64fb-105">Zestaw parametrów Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f64fb-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="f64fb-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="f64fb-106">(Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f64fb-107">Zestaw parametrów identyfikatora definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f64fb-107">The policy set definition Id parameter set.</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f64fb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f64fb-108">DESCRIPTION</span></span>
<span data-ttu-id="f64fb-109">Polecenie cmdlet **Remove-AzureRmPolicySetDefinition** usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="f64fb-109">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="f64fb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f64fb-110">EXAMPLES</span></span>

### <span data-ttu-id="f64fb-111">Przykład 1: usuwanie definicji zestawu zasad według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="f64fb-111">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="f64fb-112">Pierwsze polecenie pobiera definicję zestawu zasad za pomocą polecenia cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="f64fb-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="f64fb-113">Polecenie zapisuje je w zmiennej $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="f64fb-113">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="f64fb-114">Drugie polecenie usuwa definicję zestawu zasad określoną przez właściwość **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="f64fb-114">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="f64fb-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f64fb-115">PARAMETERS</span></span>

### <span data-ttu-id="f64fb-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f64fb-116">-ApiVersion</span></span>
<span data-ttu-id="f64fb-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="f64fb-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f64fb-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="f64fb-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f64fb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f64fb-119">-Force</span></span>
<span data-ttu-id="f64fb-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f64fb-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f64fb-121">-ID</span><span class="sxs-lookup"><span data-stu-id="f64fb-121">-Id</span></span>
<span data-ttu-id="f64fb-122">W pełni kwalifikowany identyfikator definicji zestawu zasad, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="f64fb-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="f64fb-123">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="f64fb-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="f64fb-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f64fb-124">-Name</span></span>
<span data-ttu-id="f64fb-125">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f64fb-125">The policy set definition name.</span></span>

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

### <span data-ttu-id="f64fb-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="f64fb-126">-Pre</span></span>
<span data-ttu-id="f64fb-127">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="f64fb-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f64fb-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f64fb-128">-Confirm</span></span>
<span data-ttu-id="f64fb-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f64fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f64fb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f64fb-130">-WhatIf</span></span>
<span data-ttu-id="f64fb-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f64fb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f64fb-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f64fb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f64fb-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f64fb-133">-DefaultProfile</span></span>
<span data-ttu-id="f64fb-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f64fb-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f64fb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f64fb-135">CommonParameters</span></span>
<span data-ttu-id="f64fb-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f64fb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f64fb-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f64fb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f64fb-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f64fb-138">INPUTS</span></span>

### <span data-ttu-id="f64fb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f64fb-139">System.String</span></span>

## <span data-ttu-id="f64fb-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f64fb-140">OUTPUTS</span></span>

### <span data-ttu-id="f64fb-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f64fb-141">System.Boolean</span></span>

## <span data-ttu-id="f64fb-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f64fb-142">NOTES</span></span>

## <span data-ttu-id="f64fb-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f64fb-143">RELATED LINKS</span></span>

