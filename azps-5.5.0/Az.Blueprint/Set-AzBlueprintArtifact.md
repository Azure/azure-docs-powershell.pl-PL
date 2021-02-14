---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7187994ca1e6e6ba9da3980be2e75b7b4ad1a877
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181931"
---
# <span data-ttu-id="7fb5c-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="7fb5c-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="7fb5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fb5c-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb5c-103">Aktualizowanie artefaktu w definicji planu.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="7fb5c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7fb5c-104">SYNTAX</span></span>

### <span data-ttu-id="7fb5c-105">UpdateTemplateArtifact (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7fb5c-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb5c-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="7fb5c-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb5c-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="7fb5c-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb5c-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="7fb5c-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb5c-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="7fb5c-109">DESCRIPTION</span></span>
<span data-ttu-id="7fb5c-110">Aktualizowanie artefaktu.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-110">Update an artifact.</span></span> <span data-ttu-id="7fb5c-111">Istnieją dwa sposoby aktualizowania artefaktu: za pośrednictwem artefaktu JSON jako pliku wejściowego lub przez dostarczanie parametrów w tekście tego artefaktu.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="7fb5c-112">Mimo że metoda JSON nie wymaga podania typu artefaktu w metody parametru wbudowanej, użytkownik musi podać typ artefaktu za pomocą parametru -Type.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="7fb5c-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7fb5c-113">EXAMPLES</span></span>

### <span data-ttu-id="7fb5c-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7fb5c-114">Example 1</span></span>
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

<span data-ttu-id="7fb5c-115">Aktualizowanie artefaktu za pomocą pliku JSON artefaktu.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="7fb5c-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7fb5c-116">Example 2</span></span>
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

<span data-ttu-id="7fb5c-117">Aktualizowanie artefaktu za pomocą parametrów w tekście.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="7fb5c-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7fb5c-118">Example 3</span></span>
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

<span data-ttu-id="7fb5c-119">Aktualizowanie artefaktu za pomocą ARM szablonu.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="7fb5c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fb5c-120">PARAMETERS</span></span>

### <span data-ttu-id="7fb5c-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="7fb5c-121">-ArtifactFile</span></span>
<span data-ttu-id="7fb5c-122">Lokalizacja pliku artefaktu w formacie JSON na dysku.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="7fb5c-123">—Plan</span><span class="sxs-lookup"><span data-stu-id="7fb5c-123">-Blueprint</span></span>
<span data-ttu-id="7fb5c-124">Obiekt Plan.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-124">Blueprint object.</span></span>

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

### <span data-ttu-id="7fb5c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb5c-125">-DefaultProfile</span></span>
<span data-ttu-id="7fb5c-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fb5c-127">- DependsOn</span><span class="sxs-lookup"><span data-stu-id="7fb5c-127">-DependsOn</span></span>
<span data-ttu-id="7fb5c-128">Lista nazw artefaktów, które należy utworzyć przed utworzeniam bieżącego artefaktu.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="7fb5c-129">— Opis</span><span class="sxs-lookup"><span data-stu-id="7fb5c-129">-Description</span></span>
<span data-ttu-id="7fb5c-130">Opis artefaktu.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="7fb5c-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7fb5c-131">-Name</span></span>
<span data-ttu-id="7fb5c-132">Nazwa artefaktu</span><span class="sxs-lookup"><span data-stu-id="7fb5c-132">Name of the artifact</span></span>

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

### <span data-ttu-id="7fb5c-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7fb5c-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="7fb5c-134">Identyfikator definicji definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="7fb5c-135">-PolicyDefinitionParameters</span><span class="sxs-lookup"><span data-stu-id="7fb5c-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="7fb5c-136">Hashtable of parameters to pass to the policy definition artifact.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="7fb5c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb5c-137">-ResourceGroupName</span></span>
<span data-ttu-id="7fb5c-138">Nazwa grupy zasobów, pod która ma się znaleźć artefakt.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="7fb5c-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7fb5c-139">-RoleDefinitionId</span></span>
<span data-ttu-id="7fb5c-140">Lista definicji roli</span><span class="sxs-lookup"><span data-stu-id="7fb5c-140">List of role definition</span></span>

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

### <span data-ttu-id="7fb5c-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="7fb5c-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="7fb5c-142">Lista identyfikatorów głównych definicji ról.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="7fb5c-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="7fb5c-143">-TemplateFile</span></span>
<span data-ttu-id="7fb5c-144">Lokalizacja pliku szablonu ARM na dysku.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="7fb5c-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="7fb5c-145">-TemplateParameterFile</span></span>
<span data-ttu-id="7fb5c-146">Lokalizacja pliku ARM na dysku.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="7fb5c-147">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="7fb5c-147">-Type</span></span>
<span data-ttu-id="7fb5c-148">Typ artefaktu.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-148">Type of the artifact.</span></span>
<span data-ttu-id="7fb5c-149">Obsługiwane są 3 typy: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="7fb5c-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7fb5c-150">-Confirm</span></span>
<span data-ttu-id="7fb5c-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb5c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb5c-152">-WhatIf</span></span>
<span data-ttu-id="7fb5c-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fb5c-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb5c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb5c-155">CommonParameters</span></span>
<span data-ttu-id="7fb5c-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb5c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb5c-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fb5c-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb5c-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fb5c-158">INPUTS</span></span>

### <span data-ttu-id="7fb5c-159">System.String</span><span class="sxs-lookup"><span data-stu-id="7fb5c-159">System.String</span></span>

### <span data-ttu-id="7fb5c-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="7fb5c-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="7fb5c-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="7fb5c-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="7fb5c-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7fb5c-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7fb5c-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7fb5c-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7fb5c-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7fb5c-164">System.String[]</span></span>

## <span data-ttu-id="7fb5c-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fb5c-165">OUTPUTS</span></span>

### <span data-ttu-id="7fb5c-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span><span class="sxs-lookup"><span data-stu-id="7fb5c-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="7fb5c-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7fb5c-167">NOTES</span></span>

## <span data-ttu-id="7fb5c-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7fb5c-168">RELATED LINKS</span></span>
