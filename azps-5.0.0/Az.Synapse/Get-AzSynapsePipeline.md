---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232925"
---
# <span data-ttu-id="da55d-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="da55d-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="da55d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da55d-102">SYNOPSIS</span></span>
<span data-ttu-id="da55d-103">Pobiera informacje o rurociągach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="da55d-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="da55d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da55d-104">SYNTAX</span></span>

### <span data-ttu-id="da55d-105">GetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da55d-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da55d-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="da55d-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da55d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="da55d-107">DESCRIPTION</span></span>
<span data-ttu-id="da55d-108">Polecenie cmdlet **Get-AzSynapsePipeline** pobiera informacje o rurociągach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="da55d-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="da55d-109">Jeśli określisz nazwę potoku, to polecenie cmdlet będzie pobierać informacje o tym potoku.</span><span class="sxs-lookup"><span data-stu-id="da55d-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="da55d-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich rurociągach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="da55d-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="da55d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da55d-111">EXAMPLES</span></span>

### <span data-ttu-id="da55d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da55d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="da55d-113">To polecenie pobiera informacje o wszystkich rurociągach w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="da55d-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="da55d-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="da55d-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="da55d-115">To polecenie pobiera informacje o potoku o nazwie ContosoPipeline w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="da55d-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="da55d-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="da55d-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="da55d-117">To polecenie pobiera informacje o potoku o nazwie ContosoPipeline w obszarze roboczym o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="da55d-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="da55d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da55d-118">PARAMETERS</span></span>

### <span data-ttu-id="da55d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da55d-119">-DefaultProfile</span></span>
<span data-ttu-id="da55d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da55d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da55d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da55d-121">-Name</span></span>
<span data-ttu-id="da55d-122">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="da55d-122">The pipeline name.</span></span>

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

### <span data-ttu-id="da55d-123">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="da55d-123">-WorkspaceName</span></span>
<span data-ttu-id="da55d-124">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="da55d-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="da55d-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="da55d-125">-WorkspaceObject</span></span>
<span data-ttu-id="da55d-126">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="da55d-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="da55d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da55d-127">CommonParameters</span></span>
<span data-ttu-id="da55d-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da55d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da55d-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da55d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da55d-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da55d-130">INPUTS</span></span>

### <span data-ttu-id="da55d-131">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="da55d-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="da55d-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da55d-132">OUTPUTS</span></span>

### <span data-ttu-id="da55d-133">Microsoft. Azure. Commands. Synapse. models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="da55d-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="da55d-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da55d-134">NOTES</span></span>

## <span data-ttu-id="da55d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da55d-135">RELATED LINKS</span></span>
