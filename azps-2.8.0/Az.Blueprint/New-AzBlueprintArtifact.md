---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: d33d4d5c6831b9d36062f7477c600d55040420a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706602"
---
# <span data-ttu-id="d465f-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="d465f-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="d465f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d465f-102">SYNOPSIS</span></span>
<span data-ttu-id="d465f-103">Utwórz nowy artefakt i Zapisz go w definicji plany.</span><span class="sxs-lookup"><span data-stu-id="d465f-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="d465f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d465f-104">SYNTAX</span></span>

### <span data-ttu-id="d465f-105">CreateTemplateArtifact (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d465f-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d465f-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="d465f-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d465f-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="d465f-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d465f-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="d465f-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d465f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d465f-109">DESCRIPTION</span></span>
<span data-ttu-id="d465f-110">Utwórz nowy artefakt.</span><span class="sxs-lookup"><span data-stu-id="d465f-110">Create a new artifact.</span></span> <span data-ttu-id="d465f-111">Istnieją dwa sposoby tworzenia artefaktu: za pośrednictwem notacji JSON artefaktu jako pliku wejściowego lub dostarczając parametrów w tekście artefaktu.</span><span class="sxs-lookup"><span data-stu-id="d465f-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="d465f-112">Gdy metoda JSON nie wymaga typu artefaktu, który ma zostać dostarczony w metodzie parametered, wymagane jest, aby użytkownik podał typ artefaktu za pomocą parametru-type.</span><span class="sxs-lookup"><span data-stu-id="d465f-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="d465f-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d465f-113">EXAMPLES</span></span>

### <span data-ttu-id="d465f-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d465f-114">Example 1</span></span>
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

<span data-ttu-id="d465f-115">Tworzenie nowego artefaktu za pomocą pliku JSON artefaktu.</span><span class="sxs-lookup"><span data-stu-id="d465f-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="d465f-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d465f-116">Example 2</span></span>
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

<span data-ttu-id="d465f-117">Tworzenie nowego artefaktu za pomocą parametrów wbudowanych.</span><span class="sxs-lookup"><span data-stu-id="d465f-117">Create a new artifact through inline parameters.</span></span>


### <span data-ttu-id="d465f-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d465f-118">Example 3</span></span>
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

<span data-ttu-id="d465f-119">Utwórz nowy artefakt za pomocą pliku szablonu ARM.</span><span class="sxs-lookup"><span data-stu-id="d465f-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="d465f-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d465f-120">PARAMETERS</span></span>

### <span data-ttu-id="d465f-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="d465f-121">-ArtifactFile</span></span>
<span data-ttu-id="d465f-122">Lokalizacja pliku artefaktu w formacie JSON na dysku.</span><span class="sxs-lookup"><span data-stu-id="d465f-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-123">-Plan</span><span class="sxs-lookup"><span data-stu-id="d465f-123">-Blueprint</span></span>
<span data-ttu-id="d465f-124">Obiekt plan.</span><span class="sxs-lookup"><span data-stu-id="d465f-124">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, ArtifactsByBlueprint, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d465f-125">-DefaultProfile</span></span>
<span data-ttu-id="d465f-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d465f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="d465f-127">-DependsOn</span></span>
<span data-ttu-id="d465f-128">Lista nazw artefaktów, które należy utworzyć przed utworzeniem bieżącego artefaktu.</span><span class="sxs-lookup"><span data-stu-id="d465f-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-129">— Opis</span><span class="sxs-lookup"><span data-stu-id="d465f-129">-Description</span></span>
<span data-ttu-id="d465f-130">Opis artefaktu.</span><span class="sxs-lookup"><span data-stu-id="d465f-130">Description of the artifact.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d465f-131">-Name</span></span>
<span data-ttu-id="d465f-132">Imię i nazwisko artefaktu</span><span class="sxs-lookup"><span data-stu-id="d465f-132">Name of the artifact</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateArtifactByInputFile, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d465f-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="d465f-134">Identyfikator definicji definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="d465f-134">Definition Id of the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="d465f-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="d465f-136">Obiekt Hashtable parametrów do przekazania do artefaktu definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="d465f-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d465f-137">-ResourceGroupName</span></span>
<span data-ttu-id="d465f-138">Nazwa grupy zasobów, w której ma się pojawić artefakt.</span><span class="sxs-lookup"><span data-stu-id="d465f-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d465f-139">-RoleDefinitionId</span></span>
<span data-ttu-id="d465f-140">Lista definicji ról</span><span class="sxs-lookup"><span data-stu-id="d465f-140">List of role definition</span></span>

```yaml
Type: String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="d465f-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="d465f-142">Lista identyfikatorów głównych definicji ról.</span><span class="sxs-lookup"><span data-stu-id="d465f-142">List of role definition principal ids.</span></span>

```yaml
Type: String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d465f-143">-TemplateFile</span></span>
<span data-ttu-id="d465f-144">Lokalizacja pliku szablonu ARM na dysku.</span><span class="sxs-lookup"><span data-stu-id="d465f-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="d465f-145">-TemplateParameterFile</span></span>
<span data-ttu-id="d465f-146">Lokalizacja pliku parametrów szablonu ARM na dysku.</span><span class="sxs-lookup"><span data-stu-id="d465f-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-147">-Type</span><span class="sxs-lookup"><span data-stu-id="d465f-147">-Type</span></span>
<span data-ttu-id="d465f-148">Typ artefaktu.</span><span class="sxs-lookup"><span data-stu-id="d465f-148">Type of the artifact.</span></span>
<span data-ttu-id="d465f-149">Obsługiwane są 3 typy: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="d465f-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d465f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d465f-150">CommonParameters</span></span>
<span data-ttu-id="d465f-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d465f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d465f-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d465f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d465f-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d465f-153">INPUTS</span></span>

### <span data-ttu-id="d465f-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d465f-154">System.String</span></span>

### <span data-ttu-id="d465f-155">Microsoft. Azure. Commands. plan. modele. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="d465f-155">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="d465f-156">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="d465f-156">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="d465f-157">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d465f-157">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d465f-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d465f-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d465f-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="d465f-159">System.String[]</span></span>

## <span data-ttu-id="d465f-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d465f-160">OUTPUTS</span></span>

### <span data-ttu-id="d465f-161">Microsoft. Azure. Management. plan. MODELES. artefakt</span><span class="sxs-lookup"><span data-stu-id="d465f-161">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="d465f-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d465f-162">NOTES</span></span>

## <span data-ttu-id="d465f-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d465f-163">RELATED LINKS</span></span>
