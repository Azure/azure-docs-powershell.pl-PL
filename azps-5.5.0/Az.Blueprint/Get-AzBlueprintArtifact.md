---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 725dca861c28f0194f800c80bd94d7e17efe15a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177883"
---
# <span data-ttu-id="121ba-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="121ba-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="121ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="121ba-102">SYNOPSIS</span></span>
<span data-ttu-id="121ba-103">Pobieranie artefaktów z definicji planu.</span><span class="sxs-lookup"><span data-stu-id="121ba-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="121ba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="121ba-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="121ba-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="121ba-105">DESCRIPTION</span></span>
<span data-ttu-id="121ba-106">Pobieranie artefaktów z definicji planu.</span><span class="sxs-lookup"><span data-stu-id="121ba-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="121ba-107">Jeśli wersja definicji planu nie jest określona, jest pobierana wersja robocza.</span><span class="sxs-lookup"><span data-stu-id="121ba-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="121ba-108">W przypadku, gdy nie ma wersji roboczej, jest zwracana najnowsza opublikowana definicja planu.</span><span class="sxs-lookup"><span data-stu-id="121ba-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="121ba-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="121ba-109">EXAMPLES</span></span>

### <span data-ttu-id="121ba-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="121ba-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192
```

<span data-ttu-id="121ba-111">Pobieranie artefaktów z definicji planu.</span><span class="sxs-lookup"><span data-stu-id="121ba-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="121ba-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="121ba-112">PARAMETERS</span></span>

### <span data-ttu-id="121ba-113">—Plan</span><span class="sxs-lookup"><span data-stu-id="121ba-113">-Blueprint</span></span>
<span data-ttu-id="121ba-114">Obiekt Plan.</span><span class="sxs-lookup"><span data-stu-id="121ba-114">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="121ba-115">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="121ba-115">-BlueprintVersion</span></span>
<span data-ttu-id="121ba-116">Wersja planu, z których mają pochodzić artefakty.</span><span class="sxs-lookup"><span data-stu-id="121ba-116">Version of the blueprint to get the artifacts from.</span></span>

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

### <span data-ttu-id="121ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="121ba-117">-DefaultProfile</span></span>
<span data-ttu-id="121ba-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="121ba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="121ba-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="121ba-119">-Name</span></span>
<span data-ttu-id="121ba-120">Nazwa artefaktu</span><span class="sxs-lookup"><span data-stu-id="121ba-120">Name of the artifact</span></span>

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

### <span data-ttu-id="121ba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="121ba-121">CommonParameters</span></span>
<span data-ttu-id="121ba-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="121ba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="121ba-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="121ba-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="121ba-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="121ba-124">INPUTS</span></span>

### <span data-ttu-id="121ba-125">System.String</span><span class="sxs-lookup"><span data-stu-id="121ba-125">System.String</span></span>

### <span data-ttu-id="121ba-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="121ba-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="121ba-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="121ba-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="121ba-128">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="121ba-128">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="121ba-129">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="121ba-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="121ba-130">System.String[]</span><span class="sxs-lookup"><span data-stu-id="121ba-130">System.String[]</span></span>

## <span data-ttu-id="121ba-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="121ba-131">OUTPUTS</span></span>

### <span data-ttu-id="121ba-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="121ba-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="121ba-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="121ba-133">NOTES</span></span>

## <span data-ttu-id="121ba-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="121ba-134">RELATED LINKS</span></span>
