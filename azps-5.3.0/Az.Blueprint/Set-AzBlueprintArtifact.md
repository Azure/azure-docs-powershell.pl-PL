---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7187994ca1e6e6ba9da3980be2e75b7b4ad1a877
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502047"
---
# <span data-ttu-id="44edc-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="44edc-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="44edc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44edc-102">SYNOPSIS</span></span>
<span data-ttu-id="44edc-103">Aktualizowanie artefaktu w definicji plany.</span><span class="sxs-lookup"><span data-stu-id="44edc-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="44edc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44edc-104">SYNTAX</span></span>

### <span data-ttu-id="44edc-105">UpdateTemplateArtifact (domyślny)</span><span class="sxs-lookup"><span data-stu-id="44edc-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44edc-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="44edc-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44edc-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="44edc-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44edc-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="44edc-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44edc-109">Opis</span><span class="sxs-lookup"><span data-stu-id="44edc-109">DESCRIPTION</span></span>
<span data-ttu-id="44edc-110">Aktualizowanie artefaktu.</span><span class="sxs-lookup"><span data-stu-id="44edc-110">Update an artifact.</span></span> <span data-ttu-id="44edc-111">Istnieją dwa sposoby aktualizowania artefaktu: za pośrednictwem notacji JSON artefaktu jako pliku wejściowego lub dostarczając parametrów w tekście artefaktu.</span><span class="sxs-lookup"><span data-stu-id="44edc-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="44edc-112">Gdy metoda JSON nie wymaga typu artefaktu, który ma zostać dostarczony w metodzie parametered, wymagane jest, aby użytkownik podał typ artefaktu za pomocą parametru-type.</span><span class="sxs-lookup"><span data-stu-id="44edc-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="44edc-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44edc-113">EXAMPLES</span></span>

### <span data-ttu-id="44edc-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="44edc-114">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Name PolicyStorage -Blueprint $bp -ArtifactFile C:\PolicyAssignmentStorageTag.json

DisplayName        :
Description        : Apply storage tag and the parameter also used by the template to resource groups
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/PolicyAssignmentStorageTag
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : PolicyAssignmentStorageTag
```

<span data-ttu-id="44edc-115">Aktualizowanie artefaktu za pośrednictwem pliku JSON artefaktu.</span><span class="sxs-lookup"><span data-stu-id="44edc-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="44edc-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="44edc-116">Example 2</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type PolicyAssignmentArtifact -Name "ApplyTag-RG" -Blueprint $bp -PolicyDefinitionId "/providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71" -PolicyDefinitionParameter @{tagName="[parameters('tagName')]"; tagValue="[parameters('tagValue')]"} -ResourceGroupName storageRG

DisplayName        : ApplyTag-RG
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagName,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : storageRG
Id                 : /subscriptions/28cbf98f-381d-4425-9ac4-cf342dab9753/providers/Microsoft.Blueprint/blueprints/AppNetwork/
                     artifacts/ApplyTag-RG
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : ApplyTag-RG
```

<span data-ttu-id="44edc-117">Aktualizowanie artefaktu za pomocą parametrów wbudowanych.</span><span class="sxs-lookup"><span data-stu-id="44edc-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="44edc-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="44edc-118">Example 3</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type TemplateArtifact -Name storage-account -Blueprint $bp -TemplateFile C:\StorageAccountArmTemplate.json -ResourceGroup "storageRG" -TemplateParameterFile C:\Workspace\BlueprintTemplates\RestTemplatesSomeInline\StorageAccountParameters.json

DisplayName   : storage-account
Description   :
DependsOn     :
Template      : {$schema, contentVersion, parameters, variables...}
Parameters    : {}
ResourceGroup : storageRG
Id            : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/storage-account
Type          : Microsoft.Blueprint/blueprints/artifacts
Name          : storage-account
```

<span data-ttu-id="44edc-119">Aktualizowanie artefaktu za pośrednictwem pliku szablonu ARM.</span><span class="sxs-lookup"><span data-stu-id="44edc-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="44edc-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44edc-120">PARAMETERS</span></span>

### <span data-ttu-id="44edc-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="44edc-121">-ArtifactFile</span></span>
<span data-ttu-id="44edc-122">Lokalizacja pliku artefaktu w formacie JSON na dysku.</span><span class="sxs-lookup"><span data-stu-id="44edc-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44edc-123">-Plan</span><span class="sxs-lookup"><span data-stu-id="44edc-123">-Blueprint</span></span>
<span data-ttu-id="44edc-124">Obiekt plan.</span><span class="sxs-lookup"><span data-stu-id="44edc-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44edc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44edc-125">-DefaultProfile</span></span>
<span data-ttu-id="44edc-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="44edc-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44edc-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="44edc-127">-DependsOn</span></span>
<span data-ttu-id="44edc-128">Lista nazw artefaktów, które należy utworzyć przed utworzeniem bieżącego artefaktu.</span><span class="sxs-lookup"><span data-stu-id="44edc-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44edc-129">— Opis</span><span class="sxs-lookup"><span data-stu-id="44edc-129">-Description</span></span>
<span data-ttu-id="44edc-130">Opis artefaktu.</span><span class="sxs-lookup"><span data-stu-id="44edc-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44edc-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44edc-131">-Name</span></span>
<span data-ttu-id="44edc-132">Imię i nazwisko artefaktu</span><span class="sxs-lookup"><span data-stu-id="44edc-132">Name of the artifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44edc-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="44edc-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="44edc-134">Identyfikator definicji definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="44edc-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44edc-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="44edc-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="44edc-136">Obiekt Hashtable parametrów do przekazania do artefaktu definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="44edc-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44edc-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44edc-137">-ResourceGroupName</span></span>
<span data-ttu-id="44edc-138">Nazwa grupy zasobów, w której ma się pojawić artefakt.</span><span class="sxs-lookup"><span data-stu-id="44edc-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44edc-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="44edc-139">-RoleDefinitionId</span></span>
<span data-ttu-id="44edc-140">Lista definicji ról</span><span class="sxs-lookup"><span data-stu-id="44edc-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44edc-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="44edc-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="44edc-142">Lista identyfikatorów głównych definicji ról.</span><span class="sxs-lookup"><span data-stu-id="44edc-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44edc-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="44edc-143">-TemplateFile</span></span>
<span data-ttu-id="44edc-144">Lokalizacja pliku szablonu ARM na dysku.</span><span class="sxs-lookup"><span data-stu-id="44edc-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44edc-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="44edc-145">-TemplateParameterFile</span></span>
<span data-ttu-id="44edc-146">Lokalizacja pliku parametrów szablonu ARM na dysku.</span><span class="sxs-lookup"><span data-stu-id="44edc-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44edc-147">-Type</span><span class="sxs-lookup"><span data-stu-id="44edc-147">-Type</span></span>
<span data-ttu-id="44edc-148">Typ artefaktu.</span><span class="sxs-lookup"><span data-stu-id="44edc-148">Type of the artifact.</span></span>
<span data-ttu-id="44edc-149">Obsługiwane są 3 typy: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="44edc-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44edc-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44edc-150">-Confirm</span></span>
<span data-ttu-id="44edc-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44edc-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44edc-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44edc-152">-WhatIf</span></span>
<span data-ttu-id="44edc-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44edc-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44edc-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="44edc-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44edc-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44edc-155">CommonParameters</span></span>
<span data-ttu-id="44edc-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44edc-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44edc-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44edc-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44edc-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44edc-158">INPUTS</span></span>

### <span data-ttu-id="44edc-159">System. String</span><span class="sxs-lookup"><span data-stu-id="44edc-159">System.String</span></span>

### <span data-ttu-id="44edc-160">Microsoft. Azure. Commands. plan. modele. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="44edc-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="44edc-161">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="44edc-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="44edc-162">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="44edc-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="44edc-163">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="44edc-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="44edc-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="44edc-164">System.String[]</span></span>

## <span data-ttu-id="44edc-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44edc-165">OUTPUTS</span></span>

### <span data-ttu-id="44edc-166">Microsoft. Azure. Management. plan. MODELES. artefakt</span><span class="sxs-lookup"><span data-stu-id="44edc-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="44edc-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44edc-167">NOTES</span></span>

## <span data-ttu-id="44edc-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44edc-168">RELATED LINKS</span></span>
