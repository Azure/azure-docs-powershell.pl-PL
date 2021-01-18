---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 725dca861c28f0194f800c80bd94d7e17efe15a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504240"
---
# <span data-ttu-id="7a043-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="7a043-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="7a043-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a043-102">SYNOPSIS</span></span>
<span data-ttu-id="7a043-103">Pobieranie artefaktów z definicji planów.</span><span class="sxs-lookup"><span data-stu-id="7a043-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="7a043-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a043-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a043-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a043-105">DESCRIPTION</span></span>
<span data-ttu-id="7a043-106">Pobieranie artefaktów z definicji planów.</span><span class="sxs-lookup"><span data-stu-id="7a043-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="7a043-107">Jeśli nie podano wersji definicji plany, zostanie pobrana wersja robocza.</span><span class="sxs-lookup"><span data-stu-id="7a043-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="7a043-108">W przypadku braku wersji roboczej jest zwracana Najnowsza opublikowana definicja.</span><span class="sxs-lookup"><span data-stu-id="7a043-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="7a043-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a043-109">EXAMPLES</span></span>

### <span data-ttu-id="7a043-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7a043-110">Example 1</span></span>
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

<span data-ttu-id="7a043-111">Pobieranie artefaktów z definicji planów.</span><span class="sxs-lookup"><span data-stu-id="7a043-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="7a043-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a043-112">PARAMETERS</span></span>

### <span data-ttu-id="7a043-113">-Plan</span><span class="sxs-lookup"><span data-stu-id="7a043-113">-Blueprint</span></span>
<span data-ttu-id="7a043-114">Obiekt plan.</span><span class="sxs-lookup"><span data-stu-id="7a043-114">Blueprint object.</span></span>

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

### <span data-ttu-id="7a043-115">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="7a043-115">-BlueprintVersion</span></span>
<span data-ttu-id="7a043-116">Wersja programu plan, z którego mają być pozyskane artefakty.</span><span class="sxs-lookup"><span data-stu-id="7a043-116">Version of the blueprint to get the artifacts from.</span></span>

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

### <span data-ttu-id="7a043-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a043-117">-DefaultProfile</span></span>
<span data-ttu-id="7a043-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a043-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a043-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a043-119">-Name</span></span>
<span data-ttu-id="7a043-120">Imię i nazwisko artefaktu</span><span class="sxs-lookup"><span data-stu-id="7a043-120">Name of the artifact</span></span>

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

### <span data-ttu-id="7a043-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a043-121">CommonParameters</span></span>
<span data-ttu-id="7a043-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a043-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a043-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a043-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a043-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a043-124">INPUTS</span></span>

### <span data-ttu-id="7a043-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7a043-125">System.String</span></span>

### <span data-ttu-id="7a043-126">Microsoft. Azure. Commands. plan. modele. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="7a043-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="7a043-127">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="7a043-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="7a043-128">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7a043-128">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7a043-129">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7a043-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7a043-130">System. String []</span><span class="sxs-lookup"><span data-stu-id="7a043-130">System.String[]</span></span>

## <span data-ttu-id="7a043-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a043-131">OUTPUTS</span></span>

### <span data-ttu-id="7a043-132">Microsoft. Azure. Commands. plan. modele. PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="7a043-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="7a043-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a043-133">NOTES</span></span>

## <span data-ttu-id="7a043-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a043-134">RELATED LINKS</span></span>
