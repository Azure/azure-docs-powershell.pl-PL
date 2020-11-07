---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
ms.openlocfilehash: 1096dc42ce02f3255c3c144852fc13029aebd113
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899187"
---
# <span data-ttu-id="d4dc8-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="d4dc8-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="d4dc8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="d4dc8-103">Usuwa definicję zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4dc8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4dc8-104">SYNTAX</span></span>

### <span data-ttu-id="d4dc8-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d4dc8-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4dc8-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4dc8-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4dc8-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4dc8-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4dc8-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4dc8-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4dc8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d4dc8-109">DESCRIPTION</span></span>
<span data-ttu-id="d4dc8-110">Polecenie cmdlet **Remove-AzureRmPolicySetDefinition** usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-110">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="d4dc8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4dc8-111">EXAMPLES</span></span>

### <span data-ttu-id="d4dc8-112">Przykład 1: usuwanie definicji zestawu zasad według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="d4dc8-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="d4dc8-113">Pierwsze polecenie pobiera definicję zestawu zasad za pomocą polecenia cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="d4dc8-114">Polecenie zapisuje je w zmiennej $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="d4dc8-115">Drugie polecenie usuwa definicję zestawu zasad określoną przez właściwość **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="d4dc8-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4dc8-116">PARAMETERS</span></span>

### <span data-ttu-id="d4dc8-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d4dc8-117">-ApiVersion</span></span>
<span data-ttu-id="d4dc8-118">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d4dc8-119">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d4dc8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4dc8-120">-DefaultProfile</span></span>
<span data-ttu-id="d4dc8-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d4dc8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4dc8-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d4dc8-122">-Force</span></span>
<span data-ttu-id="d4dc8-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d4dc8-124">-ID</span><span class="sxs-lookup"><span data-stu-id="d4dc8-124">-Id</span></span>
<span data-ttu-id="d4dc8-125">W pełni kwalifikowany identyfikator definicji zestawu zasad, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="d4dc8-126">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="d4dc8-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="d4dc8-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d4dc8-127">-ManagementGroupName</span></span>
<span data-ttu-id="d4dc8-128">Nazwa grupy zarządzania definicji zestawu zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-128">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="d4dc8-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d4dc8-129">-Name</span></span>
<span data-ttu-id="d4dc8-130">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-130">The policy set definition name.</span></span>

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

### <span data-ttu-id="d4dc8-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="d4dc8-131">-Pre</span></span>
<span data-ttu-id="d4dc8-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d4dc8-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d4dc8-133">-SubscriptionId</span></span>
<span data-ttu-id="d4dc8-134">Identyfikator subskrypcji definicji zestawu zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-134">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="d4dc8-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4dc8-135">-Confirm</span></span>
<span data-ttu-id="d4dc8-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4dc8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4dc8-137">-WhatIf</span></span>
<span data-ttu-id="d4dc8-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4dc8-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4dc8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4dc8-140">CommonParameters</span></span>
<span data-ttu-id="d4dc8-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4dc8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4dc8-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4dc8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4dc8-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4dc8-143">INPUTS</span></span>

### <span data-ttu-id="d4dc8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d4dc8-144">System.String</span></span>

### <span data-ttu-id="d4dc8-145">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d4dc8-145">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d4dc8-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4dc8-146">OUTPUTS</span></span>

### <span data-ttu-id="d4dc8-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4dc8-147">System.Boolean</span></span>

## <span data-ttu-id="d4dc8-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4dc8-148">NOTES</span></span>

## <span data-ttu-id="d4dc8-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4dc8-149">RELATED LINKS</span></span>
