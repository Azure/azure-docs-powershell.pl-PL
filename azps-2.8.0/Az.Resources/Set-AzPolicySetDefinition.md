---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 5b6d514fc41c909fdd48b6a13ba85ab5836a5668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873268"
---
# <span data-ttu-id="59547-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="59547-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="59547-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59547-102">SYNOPSIS</span></span>
<span data-ttu-id="59547-103">Modyfikowanie definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="59547-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="59547-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59547-104">SYNTAX</span></span>

### <span data-ttu-id="59547-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="59547-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59547-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="59547-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59547-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59547-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59547-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59547-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59547-109">Opis</span><span class="sxs-lookup"><span data-stu-id="59547-109">DESCRIPTION</span></span>
<span data-ttu-id="59547-110">Polecenie cmdlet **Set-AzPolicySetDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="59547-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="59547-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59547-111">EXAMPLES</span></span>

### <span data-ttu-id="59547-112">Przykład 1: aktualizowanie opisu definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="59547-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="59547-113">Pierwsze polecenie pobiera definicję zestawu zasad za pomocą polecenia cmdlet Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="59547-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="59547-114">Polecenie zapisuje ten obiekt w zmiennej $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="59547-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="59547-115">Drugie polecenie aktualizuje opis definicji zestawu zasad określonego przez właściwość **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="59547-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="59547-116">Przykład 2: aktualizowanie metadanych definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="59547-116">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="59547-117">To polecenie powoduje zaktualizowanie metadanych definicji zestawu zasad o nazwie VMPolicySetDefinition w celu wskazania jej kategorii "maszyna wirtualna".</span><span class="sxs-lookup"><span data-stu-id="59547-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="59547-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59547-118">PARAMETERS</span></span>

### <span data-ttu-id="59547-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="59547-119">-ApiVersion</span></span>
<span data-ttu-id="59547-120">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="59547-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="59547-121">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="59547-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="59547-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59547-122">-DefaultProfile</span></span>
<span data-ttu-id="59547-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="59547-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59547-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="59547-124">-Description</span></span>
<span data-ttu-id="59547-125">Opis definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="59547-125">The description for policy set definition.</span></span>

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

### <span data-ttu-id="59547-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="59547-126">-DisplayName</span></span>
<span data-ttu-id="59547-127">Nazwa wyświetlana definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="59547-127">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="59547-128">-ID</span><span class="sxs-lookup"><span data-stu-id="59547-128">-Id</span></span>
<span data-ttu-id="59547-129">Identyfikator definicji zasad w pełni kwalifikowany, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="59547-129">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="59547-130">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="59547-130">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="59547-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="59547-131">-ManagementGroupName</span></span>
<span data-ttu-id="59547-132">Nazwa grupy zarządzania definicji zestawu zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="59547-132">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="59547-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="59547-133">-Metadata</span></span>
<span data-ttu-id="59547-134">Metadane zaktualizowanej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="59547-134">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="59547-135">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="59547-135">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="59547-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="59547-136">-Name</span></span>
<span data-ttu-id="59547-137">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="59547-137">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59547-138">-Parameter</span><span class="sxs-lookup"><span data-stu-id="59547-138">-Parameter</span></span>
<span data-ttu-id="59547-139">Deklaracja parametrów zaktualizowanej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="59547-139">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="59547-140">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego deklarację Parameters lub deklaracji Parameters jako ciągu.</span><span class="sxs-lookup"><span data-stu-id="59547-140">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="59547-141">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="59547-141">-PolicyDefinition</span></span>
<span data-ttu-id="59547-142">Definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="59547-142">The policy definitions.</span></span> <span data-ttu-id="59547-143">Może to być ścieżka do nazwy pliku zawierającej definicje zasad lub definicje zasad jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="59547-143">This can either be a path to a file name containing the policy definitions, or the policy definitions as string.</span></span>

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

### <span data-ttu-id="59547-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="59547-144">-Pre</span></span>
<span data-ttu-id="59547-145">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="59547-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="59547-146">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="59547-146">-SubscriptionId</span></span>
<span data-ttu-id="59547-147">Identyfikator subskrypcji definicji zestawu zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="59547-147">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="59547-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59547-148">-Confirm</span></span>
<span data-ttu-id="59547-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59547-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59547-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59547-150">-WhatIf</span></span>
<span data-ttu-id="59547-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59547-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59547-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="59547-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59547-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59547-153">CommonParameters</span></span>
<span data-ttu-id="59547-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59547-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59547-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59547-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59547-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59547-156">INPUTS</span></span>

### <span data-ttu-id="59547-157">System. String</span><span class="sxs-lookup"><span data-stu-id="59547-157">System.String</span></span>

### <span data-ttu-id="59547-158">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="59547-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="59547-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59547-159">OUTPUTS</span></span>

### <span data-ttu-id="59547-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="59547-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="59547-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59547-161">NOTES</span></span>

## <span data-ttu-id="59547-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59547-162">RELATED LINKS</span></span>
