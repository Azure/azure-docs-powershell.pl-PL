---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 3174f56a0488b196dc3dc330cfa6435def73476c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708302"
---
# <span data-ttu-id="7672e-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="7672e-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="7672e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7672e-102">SYNOPSIS</span></span>
<span data-ttu-id="7672e-103">Usuwa definicję zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="7672e-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="7672e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7672e-104">SYNTAX</span></span>

### <span data-ttu-id="7672e-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7672e-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7672e-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7672e-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7672e-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7672e-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7672e-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7672e-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7672e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7672e-109">DESCRIPTION</span></span>
<span data-ttu-id="7672e-110">Polecenie cmdlet **Remove-AzPolicySetDefinition** usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="7672e-110">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="7672e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7672e-111">EXAMPLES</span></span>

### <span data-ttu-id="7672e-112">Przykład 1: usuwanie definicji zestawu zasad według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="7672e-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="7672e-113">Pierwsze polecenie pobiera definicję zestawu zasad za pomocą polecenia cmdlet Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="7672e-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="7672e-114">Polecenie zapisuje je w zmiennej $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="7672e-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="7672e-115">Drugie polecenie usuwa definicję zestawu zasad określoną przez właściwość **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="7672e-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="7672e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7672e-116">PARAMETERS</span></span>

### <span data-ttu-id="7672e-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7672e-117">-ApiVersion</span></span>
<span data-ttu-id="7672e-118">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="7672e-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7672e-119">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="7672e-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="7672e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7672e-120">-DefaultProfile</span></span>
<span data-ttu-id="7672e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7672e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7672e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7672e-122">-Force</span></span>
<span data-ttu-id="7672e-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7672e-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7672e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="7672e-124">-Id</span></span>
<span data-ttu-id="7672e-125">W pełni kwalifikowany identyfikator definicji zestawu zasad, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="7672e-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="7672e-126">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="7672e-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="7672e-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="7672e-127">-ManagementGroupName</span></span>
<span data-ttu-id="7672e-128">Nazwa grupy zarządzania definicji zestawu zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="7672e-128">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="7672e-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7672e-129">-Name</span></span>
<span data-ttu-id="7672e-130">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="7672e-130">The policy set definition name.</span></span>

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

### <span data-ttu-id="7672e-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="7672e-131">-Pre</span></span>
<span data-ttu-id="7672e-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="7672e-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7672e-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7672e-133">-SubscriptionId</span></span>
<span data-ttu-id="7672e-134">Identyfikator subskrypcji definicji zestawu zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="7672e-134">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="7672e-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7672e-135">-Confirm</span></span>
<span data-ttu-id="7672e-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7672e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7672e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7672e-137">-WhatIf</span></span>
<span data-ttu-id="7672e-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7672e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7672e-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7672e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7672e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7672e-140">CommonParameters</span></span>
<span data-ttu-id="7672e-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7672e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7672e-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7672e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7672e-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7672e-143">INPUTS</span></span>

### <span data-ttu-id="7672e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7672e-144">System.String</span></span>

### <span data-ttu-id="7672e-145">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7672e-145">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7672e-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7672e-146">OUTPUTS</span></span>

### <span data-ttu-id="7672e-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7672e-147">System.Boolean</span></span>

## <span data-ttu-id="7672e-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7672e-148">NOTES</span></span>

## <span data-ttu-id="7672e-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7672e-149">RELATED LINKS</span></span>
