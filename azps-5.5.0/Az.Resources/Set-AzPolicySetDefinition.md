---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: cd8bc24a0cedac91ef18e19a80e1662fdcbac297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201811"
---
# <span data-ttu-id="06bd1-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="06bd1-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="06bd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="06bd1-103">Modyfikuje definicję zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="06bd1-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="06bd1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06bd1-104">SYNTAX</span></span>

### <span data-ttu-id="06bd1-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="06bd1-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06bd1-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="06bd1-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06bd1-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06bd1-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06bd1-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06bd1-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06bd1-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06bd1-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06bd1-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="06bd1-110">DESCRIPTION</span></span>
<span data-ttu-id="06bd1-111">Polecenie **cmdlet Set-AzPolicySetDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="06bd1-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="06bd1-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06bd1-112">EXAMPLES</span></span>

### <span data-ttu-id="06bd1-113">Przykład 1. Aktualizowanie opisu definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="06bd1-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="06bd1-114">Pierwsze polecenie otrzymuje definicję zestawu zasad przy użyciu Get-AzPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06bd1-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="06bd1-115">Polecenie przechowuje ten obiekt w $PolicySetDefinition zmienną.</span><span class="sxs-lookup"><span data-stu-id="06bd1-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="06bd1-116">Drugie polecenie aktualizuje opis definicji zestawu zasad zidentyfikowanych przez właściwość **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="06bd1-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="06bd1-117">Przykład 2. Aktualizowanie metadanych definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="06bd1-117">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="06bd1-118">To polecenie aktualizuje metadane definicji zestawu zasad o nazwie VMPolicySetDefinition, aby wskazać, że jej kategoria to "Maszyny wirtualne".</span><span class="sxs-lookup"><span data-stu-id="06bd1-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="06bd1-119">Przykład 3. Aktualizowanie grup definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="06bd1-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="06bd1-120">To polecenie aktualizuje grupy definicji zestawu zasad o nazwie VMPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="06bd1-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="06bd1-121">Przykład 4. Aktualizowanie grup definicji zestawu zasad przy użyciu tabeli skrótów</span><span class="sxs-lookup"><span data-stu-id="06bd1-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="06bd1-122">To polecenie aktualizuje grupy definicji zestawu zasad o nazwie VMPolicySetDefinition, używając tabeli skrótów do konstruowania grup.</span><span class="sxs-lookup"><span data-stu-id="06bd1-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="06bd1-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06bd1-123">PARAMETERS</span></span>

### <span data-ttu-id="06bd1-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="06bd1-124">-ApiVersion</span></span>
<span data-ttu-id="06bd1-125">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="06bd1-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="06bd1-126">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="06bd1-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="06bd1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06bd1-127">-DefaultProfile</span></span>
<span data-ttu-id="06bd1-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="06bd1-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06bd1-129">— Opis</span><span class="sxs-lookup"><span data-stu-id="06bd1-129">-Description</span></span>
<span data-ttu-id="06bd1-130">Opis definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="06bd1-130">The description for policy set definition.</span></span>

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

### <span data-ttu-id="06bd1-131">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="06bd1-131">-DisplayName</span></span>
<span data-ttu-id="06bd1-132">Nazwa wyświetlana definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="06bd1-132">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="06bd1-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="06bd1-133">-GroupDefinition</span></span>
<span data-ttu-id="06bd1-134">Grupy definicji zasad w definicji zaktualizowanego zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="06bd1-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="06bd1-135">Może to być ścieżka do pliku zawierającego grupy lub grupy jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="06bd1-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="06bd1-136">— Id</span><span class="sxs-lookup"><span data-stu-id="06bd1-136">-Id</span></span>
<span data-ttu-id="06bd1-137">W pełni kwalifikowany identyfikator definicji zasad, łącznie z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="06bd1-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="06bd1-138">np. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="06bd1-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="06bd1-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06bd1-139">-InputObject</span></span>
<span data-ttu-id="06bd1-140">Zasady ustawiają obiekt definicji w celu aktualizowania danych wyjściowych z innego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06bd1-140">The policy set definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="06bd1-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="06bd1-141">-ManagementGroupName</span></span>
<span data-ttu-id="06bd1-142">Nazwa grupy zarządzania definicji zestawu zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="06bd1-142">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="06bd1-143">— Metadane</span><span class="sxs-lookup"><span data-stu-id="06bd1-143">-Metadata</span></span>
<span data-ttu-id="06bd1-144">Metadane definicji zaktualizowanego zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="06bd1-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="06bd1-145">Może to być ścieżka do nazwy pliku zawierającej metadane lub metadane jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="06bd1-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="06bd1-146">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="06bd1-146">-Name</span></span>
<span data-ttu-id="06bd1-147">Nazwa definicji ustawiona przez zasady.</span><span class="sxs-lookup"><span data-stu-id="06bd1-147">The policy set definition name.</span></span>

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

### <span data-ttu-id="06bd1-148">- Parametr</span><span class="sxs-lookup"><span data-stu-id="06bd1-148">-Parameter</span></span>
<span data-ttu-id="06bd1-149">Deklaracja parametrów definicji zaktualizowanego zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="06bd1-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="06bd1-150">Może to być ścieżka do nazwy pliku lub uri zawierającej deklarację parametrów albo deklaracja parametrów jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="06bd1-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="06bd1-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="06bd1-151">-PolicyDefinition</span></span>
<span data-ttu-id="06bd1-152">Definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="06bd1-152">The policy definitions.</span></span> <span data-ttu-id="06bd1-153">Może to być ścieżka do nazwy pliku zawierającej definicje zasad lub definicje zasad jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="06bd1-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="06bd1-154">— Przed</span><span class="sxs-lookup"><span data-stu-id="06bd1-154">-Pre</span></span>
<span data-ttu-id="06bd1-155">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="06bd1-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="06bd1-156">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06bd1-156">-SubscriptionId</span></span>
<span data-ttu-id="06bd1-157">Identyfikator subskrypcji definicji zestawu zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="06bd1-157">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="06bd1-158">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06bd1-158">-Confirm</span></span>
<span data-ttu-id="06bd1-159">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06bd1-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06bd1-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06bd1-160">-WhatIf</span></span>
<span data-ttu-id="06bd1-161">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06bd1-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06bd1-162">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="06bd1-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06bd1-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06bd1-163">CommonParameters</span></span>
<span data-ttu-id="06bd1-164">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06bd1-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06bd1-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06bd1-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06bd1-166">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06bd1-166">INPUTS</span></span>

### <span data-ttu-id="06bd1-167">System.String</span><span class="sxs-lookup"><span data-stu-id="06bd1-167">System.String</span></span>

### <span data-ttu-id="06bd1-168">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="06bd1-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="06bd1-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="06bd1-169">OUTPUTS</span></span>

### <span data-ttu-id="06bd1-170">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="06bd1-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="06bd1-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06bd1-171">NOTES</span></span>

## <span data-ttu-id="06bd1-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06bd1-172">RELATED LINKS</span></span>
