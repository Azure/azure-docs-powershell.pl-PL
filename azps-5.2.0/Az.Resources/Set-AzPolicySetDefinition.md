---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: cd8bc24a0cedac91ef18e19a80e1662fdcbac297
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351733"
---
# <span data-ttu-id="1b989-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1b989-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="1b989-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b989-102">SYNOPSIS</span></span>
<span data-ttu-id="1b989-103">Modyfikowanie definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="1b989-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="1b989-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b989-104">SYNTAX</span></span>

### <span data-ttu-id="1b989-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1b989-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b989-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b989-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b989-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b989-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b989-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b989-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b989-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b989-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b989-110">Opis</span><span class="sxs-lookup"><span data-stu-id="1b989-110">DESCRIPTION</span></span>
<span data-ttu-id="1b989-111">Polecenie cmdlet **Set-AzPolicySetDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="1b989-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="1b989-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b989-112">EXAMPLES</span></span>

### <span data-ttu-id="1b989-113">Przykład 1: aktualizowanie opisu definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="1b989-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="1b989-114">Pierwsze polecenie pobiera definicję zestawu zasad za pomocą polecenia cmdlet Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="1b989-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="1b989-115">Polecenie zapisuje ten obiekt w zmiennej $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="1b989-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="1b989-116">Drugie polecenie aktualizuje opis definicji zestawu zasad określonego przez właściwość **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="1b989-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="1b989-117">Przykład 2: aktualizowanie metadanych definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="1b989-117">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="1b989-118">To polecenie powoduje zaktualizowanie metadanych definicji zestawu zasad o nazwie VMPolicySetDefinition w celu wskazania jej kategorii "maszyna wirtualna".</span><span class="sxs-lookup"><span data-stu-id="1b989-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="1b989-119">Przykład 3: aktualizowanie grup definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="1b989-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="1b989-120">To polecenie aktualizuje grupy definicji zestawu zasad o nazwie VMPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="1b989-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="1b989-121">Przykład 4: aktualizowanie grup definicji zestawu zasad przy użyciu tabeli skrótów</span><span class="sxs-lookup"><span data-stu-id="1b989-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="1b989-122">To polecenie aktualizuje grupy definicji zestawu zasad o nazwie VMPolicySetDefinition przy użyciu tablicy skrótów do konstruowania grup.</span><span class="sxs-lookup"><span data-stu-id="1b989-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="1b989-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b989-123">PARAMETERS</span></span>

### <span data-ttu-id="1b989-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1b989-124">-ApiVersion</span></span>
<span data-ttu-id="1b989-125">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="1b989-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1b989-126">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="1b989-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1b989-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b989-127">-DefaultProfile</span></span>
<span data-ttu-id="1b989-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1b989-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b989-129">— Opis</span><span class="sxs-lookup"><span data-stu-id="1b989-129">-Description</span></span>
<span data-ttu-id="1b989-130">Opis definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="1b989-130">The description for policy set definition.</span></span>

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

### <span data-ttu-id="1b989-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1b989-131">-DisplayName</span></span>
<span data-ttu-id="1b989-132">Nazwa wyświetlana definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="1b989-132">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="1b989-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="1b989-133">-GroupDefinition</span></span>
<span data-ttu-id="1b989-134">Grupy definicji zasad zaktualizowanej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="1b989-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="1b989-135">Może to być ścieżka do pliku zawierającego grupy lub grupy jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="1b989-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="1b989-136">-ID</span><span class="sxs-lookup"><span data-stu-id="1b989-136">-Id</span></span>
<span data-ttu-id="1b989-137">Identyfikator definicji zasad w pełni kwalifikowany, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="1b989-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="1b989-138">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1b989-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="1b989-139">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1b989-139">-InputObject</span></span>
<span data-ttu-id="1b989-140">Obiekt definicji zestawu zasad do zaktualizowania, który został wyprowadzony z innego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b989-140">The policy set definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b989-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1b989-141">-ManagementGroupName</span></span>
<span data-ttu-id="1b989-142">Nazwa grupy zarządzania definicji zestawu zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="1b989-142">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="1b989-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1b989-143">-Metadata</span></span>
<span data-ttu-id="1b989-144">Metadane zaktualizowanej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="1b989-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="1b989-145">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="1b989-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="1b989-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b989-146">-Name</span></span>
<span data-ttu-id="1b989-147">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="1b989-147">The policy set definition name.</span></span>

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

### <span data-ttu-id="1b989-148">-Parameter</span><span class="sxs-lookup"><span data-stu-id="1b989-148">-Parameter</span></span>
<span data-ttu-id="1b989-149">Deklaracja parametrów zaktualizowanej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="1b989-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="1b989-150">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego deklarację Parameters lub deklaracji Parameters jako ciągu JSON.</span><span class="sxs-lookup"><span data-stu-id="1b989-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="1b989-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1b989-151">-PolicyDefinition</span></span>
<span data-ttu-id="1b989-152">Definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="1b989-152">The policy definitions.</span></span> <span data-ttu-id="1b989-153">Może to być ścieżka do nazwy pliku zawierającego definicje zasad lub definicje zasad jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="1b989-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="1b989-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="1b989-154">-Pre</span></span>
<span data-ttu-id="1b989-155">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="1b989-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1b989-156">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1b989-156">-SubscriptionId</span></span>
<span data-ttu-id="1b989-157">Identyfikator subskrypcji definicji zestawu zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="1b989-157">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="1b989-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b989-158">-Confirm</span></span>
<span data-ttu-id="1b989-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b989-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b989-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b989-160">-WhatIf</span></span>
<span data-ttu-id="1b989-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b989-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b989-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b989-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b989-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b989-163">CommonParameters</span></span>
<span data-ttu-id="1b989-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b989-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b989-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b989-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b989-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b989-166">INPUTS</span></span>

### <span data-ttu-id="1b989-167">System. String</span><span class="sxs-lookup"><span data-stu-id="1b989-167">System.String</span></span>

### <span data-ttu-id="1b989-168">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1b989-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1b989-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b989-169">OUTPUTS</span></span>

### <span data-ttu-id="1b989-170">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1b989-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1b989-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b989-171">NOTES</span></span>

## <span data-ttu-id="1b989-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b989-172">RELATED LINKS</span></span>
