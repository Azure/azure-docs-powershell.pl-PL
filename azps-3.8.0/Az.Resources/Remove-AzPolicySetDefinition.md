---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: c74f27eab090f03435758697f71774af88493367
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050725"
---
# <span data-ttu-id="da366-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="da366-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="da366-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da366-102">SYNOPSIS</span></span>
<span data-ttu-id="da366-103">Usuwa definicję zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="da366-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="da366-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da366-104">SYNTAX</span></span>

### <span data-ttu-id="da366-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da366-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da366-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="da366-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da366-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da366-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da366-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da366-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da366-109">Opis</span><span class="sxs-lookup"><span data-stu-id="da366-109">DESCRIPTION</span></span>
<span data-ttu-id="da366-110">Polecenie cmdlet **Remove-AzPolicySetDefinition** usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="da366-110">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="da366-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da366-111">EXAMPLES</span></span>

### <span data-ttu-id="da366-112">Przykład 1: usuwanie definicji zestawu zasad według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="da366-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="da366-113">Pierwsze polecenie pobiera definicję zestawu zasad za pomocą polecenia cmdlet Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="da366-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="da366-114">Polecenie zapisuje je w zmiennej $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="da366-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="da366-115">Drugie polecenie usuwa definicję zestawu zasad określoną przez właściwość **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="da366-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="da366-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da366-116">PARAMETERS</span></span>

### <span data-ttu-id="da366-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="da366-117">-ApiVersion</span></span>
<span data-ttu-id="da366-118">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="da366-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="da366-119">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="da366-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="da366-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da366-120">-DefaultProfile</span></span>
<span data-ttu-id="da366-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="da366-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da366-122">-Force</span><span class="sxs-lookup"><span data-stu-id="da366-122">-Force</span></span>
<span data-ttu-id="da366-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="da366-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="da366-124">-ID</span><span class="sxs-lookup"><span data-stu-id="da366-124">-Id</span></span>
<span data-ttu-id="da366-125">W pełni kwalifikowany identyfikator definicji zestawu zasad, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="da366-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="da366-126">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="da366-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da366-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="da366-127">-ManagementGroupName</span></span>
<span data-ttu-id="da366-128">Nazwa grupy zarządzania definicji zestawu zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="da366-128">The name of the management group of the policy set definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da366-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da366-129">-Name</span></span>
<span data-ttu-id="da366-130">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="da366-130">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da366-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="da366-131">-Pre</span></span>
<span data-ttu-id="da366-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="da366-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="da366-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da366-133">-SubscriptionId</span></span>
<span data-ttu-id="da366-134">Identyfikator subskrypcji definicji zestawu zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="da366-134">The subscription ID of the policy set definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da366-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da366-135">-Confirm</span></span>
<span data-ttu-id="da366-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da366-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da366-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da366-137">-WhatIf</span></span>
<span data-ttu-id="da366-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da366-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da366-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da366-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da366-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da366-140">CommonParameters</span></span>
<span data-ttu-id="da366-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da366-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da366-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da366-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da366-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da366-143">INPUTS</span></span>

### <span data-ttu-id="da366-144">System. String</span><span class="sxs-lookup"><span data-stu-id="da366-144">System.String</span></span>

### <span data-ttu-id="da366-145">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="da366-145">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="da366-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da366-146">OUTPUTS</span></span>

### <span data-ttu-id="da366-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da366-147">System.Boolean</span></span>

## <span data-ttu-id="da366-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da366-148">NOTES</span></span>

## <span data-ttu-id="da366-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da366-149">RELATED LINKS</span></span>
