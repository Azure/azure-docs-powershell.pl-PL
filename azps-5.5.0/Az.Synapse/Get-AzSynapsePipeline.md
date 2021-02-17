---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241746"
---
# <span data-ttu-id="bc373-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="bc373-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="bc373-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc373-102">SYNOPSIS</span></span>
<span data-ttu-id="bc373-103">Pobiera informacje o potokach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="bc373-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="bc373-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bc373-104">SYNTAX</span></span>

### <span data-ttu-id="bc373-105">GetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="bc373-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc373-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="bc373-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc373-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bc373-107">DESCRIPTION</span></span>
<span data-ttu-id="bc373-108">Polecenie **cmdlet Get-AzSynapsePipeline** pobiera informacje o potokach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="bc373-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="bc373-109">Jeśli określisz nazwę potoku, to polecenie cmdlet pobiera informacje o tym potoku.</span><span class="sxs-lookup"><span data-stu-id="bc373-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="bc373-110">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich potokach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="bc373-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="bc373-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bc373-111">EXAMPLES</span></span>

### <span data-ttu-id="bc373-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bc373-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="bc373-113">To polecenie pobiera informacje o wszystkich potokach w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="bc373-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="bc373-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bc373-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="bc373-115">To polecenie pobiera informacje o potoku o nazwie ContosoPipeline w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="bc373-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="bc373-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="bc373-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="bc373-117">To polecenie pobiera informacje o potoku o nazwie ContosoPipeline w obszarze roboczym o nazwie ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="bc373-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="bc373-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc373-118">PARAMETERS</span></span>

### <span data-ttu-id="bc373-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc373-119">-DefaultProfile</span></span>
<span data-ttu-id="bc373-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc373-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc373-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bc373-121">-Name</span></span>
<span data-ttu-id="bc373-122">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="bc373-122">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc373-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bc373-123">-WorkspaceName</span></span>
<span data-ttu-id="bc373-124">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="bc373-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bc373-125">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bc373-125">-WorkspaceObject</span></span>
<span data-ttu-id="bc373-126">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="bc373-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bc373-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc373-127">CommonParameters</span></span>
<span data-ttu-id="bc373-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc373-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc373-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc373-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc373-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc373-130">INPUTS</span></span>

### <span data-ttu-id="bc373-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bc373-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="bc373-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc373-132">OUTPUTS</span></span>

### <span data-ttu-id="bc373-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="bc373-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="bc373-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bc373-134">NOTES</span></span>

## <span data-ttu-id="bc373-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc373-135">RELATED LINKS</span></span>
