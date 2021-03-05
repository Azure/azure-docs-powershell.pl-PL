---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 988d2f53ebf0bf69806bf06fedb5e2db31c9d0c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973066"
---
# <span data-ttu-id="a8da0-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="a8da0-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="a8da0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8da0-102">SYNOPSIS</span></span>
<span data-ttu-id="a8da0-103">Pobiera informacje o wyzwalaczach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a8da0-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="a8da0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a8da0-104">SYNTAX</span></span>

### <span data-ttu-id="a8da0-105">GetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="a8da0-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8da0-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="a8da0-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8da0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a8da0-107">DESCRIPTION</span></span>
<span data-ttu-id="a8da0-108">Polecenie **cmdlet Get-AzSynapseTrigger** pobiera informacje o wyzwalaczach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a8da0-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="a8da0-109">Jeśli określisz nazwę wyzwalacza, polecenie cmdlet pobiera informacje o tym wyzwalaczu.</span><span class="sxs-lookup"><span data-stu-id="a8da0-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="a8da0-110">Jeśli nie określisz nazwy, polecenie cmdlet pobiera informacje o wszystkich wyzwalaczach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a8da0-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="a8da0-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a8da0-111">EXAMPLES</span></span>

### <span data-ttu-id="a8da0-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a8da0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a8da0-113">Pobiera listę wszystkich wyzwalaczy utworzonych w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a8da0-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a8da0-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a8da0-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="a8da0-115">Pobiera pojedynczy wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a8da0-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a8da0-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a8da0-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="a8da0-117">Pobiera pojedynczy wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="a8da0-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a8da0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8da0-118">PARAMETERS</span></span>

### <span data-ttu-id="a8da0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8da0-119">-DefaultProfile</span></span>
<span data-ttu-id="a8da0-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8da0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8da0-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a8da0-121">-Name</span></span>
<span data-ttu-id="a8da0-122">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="a8da0-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8da0-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a8da0-123">-WorkspaceName</span></span>
<span data-ttu-id="a8da0-124">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="a8da0-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8da0-125">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a8da0-125">-WorkspaceObject</span></span>
<span data-ttu-id="a8da0-126">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="a8da0-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8da0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8da0-127">CommonParameters</span></span>
<span data-ttu-id="a8da0-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8da0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8da0-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8da0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8da0-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8da0-130">INPUTS</span></span>

### <span data-ttu-id="a8da0-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a8da0-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a8da0-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8da0-132">OUTPUTS</span></span>

### <span data-ttu-id="a8da0-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="a8da0-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="a8da0-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a8da0-134">NOTES</span></span>

## <span data-ttu-id="a8da0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8da0-135">RELATED LINKS</span></span>
