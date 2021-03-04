---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 0fa0069686a34fbd1ee60d31df96386a5d7959d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981850"
---
# <span data-ttu-id="a53ff-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="a53ff-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="a53ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a53ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a53ff-103">Pobiera informacje o przepływach danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a53ff-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="a53ff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a53ff-104">SYNTAX</span></span>

### <span data-ttu-id="a53ff-105">GetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="a53ff-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a53ff-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="a53ff-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a53ff-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a53ff-107">DESCRIPTION</span></span>
<span data-ttu-id="a53ff-108">Polecenie **cmdlet Get-AzSynapseDataFlow** pobiera informacje o przepływach danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a53ff-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="a53ff-109">Jeśli określisz nazwę przepływu danych, to polecenie cmdlet pobiera informacje o tym przepływie danych.</span><span class="sxs-lookup"><span data-stu-id="a53ff-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="a53ff-110">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich przepływach danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a53ff-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="a53ff-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a53ff-111">EXAMPLES</span></span>

### <span data-ttu-id="a53ff-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a53ff-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a53ff-113">To polecenie pobiera informacje o wszystkich przepływach danych w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a53ff-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a53ff-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a53ff-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="a53ff-115">To polecenie pobiera informacje o przepływie danych o nazwie ContosoDataFlow w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a53ff-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a53ff-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a53ff-116">PARAMETERS</span></span>

### <span data-ttu-id="a53ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a53ff-117">-DefaultProfile</span></span>
<span data-ttu-id="a53ff-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a53ff-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a53ff-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a53ff-119">-Name</span></span>
<span data-ttu-id="a53ff-120">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="a53ff-120">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ff-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a53ff-121">-WorkspaceName</span></span>
<span data-ttu-id="a53ff-122">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="a53ff-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a53ff-123">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a53ff-123">-WorkspaceObject</span></span>
<span data-ttu-id="a53ff-124">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="a53ff-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a53ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a53ff-125">CommonParameters</span></span>
<span data-ttu-id="a53ff-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a53ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a53ff-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a53ff-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a53ff-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a53ff-128">INPUTS</span></span>

### <span data-ttu-id="a53ff-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a53ff-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a53ff-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a53ff-130">OUTPUTS</span></span>

### <span data-ttu-id="a53ff-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="a53ff-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="a53ff-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a53ff-132">NOTES</span></span>

## <span data-ttu-id="a53ff-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a53ff-133">RELATED LINKS</span></span>
