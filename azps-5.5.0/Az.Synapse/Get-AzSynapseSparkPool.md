---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188803"
---
# <span data-ttu-id="12e42-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="12e42-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="12e42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e42-102">SYNOPSIS</span></span>
<span data-ttu-id="12e42-103">Pobiera pulę przebiegu w czasie analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="12e42-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="12e42-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="12e42-104">SYNTAX</span></span>

### <span data-ttu-id="12e42-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="12e42-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12e42-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12e42-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12e42-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12e42-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12e42-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="12e42-108">DESCRIPTION</span></span>
<span data-ttu-id="12e42-109">Polecenie **cmdlet Get-AzSynapseSparkPool** pobiera informacje o puli przebiegu w czasie usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="12e42-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="12e42-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="12e42-110">EXAMPLES</span></span>

### <span data-ttu-id="12e42-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="12e42-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="12e42-112">To polecenie pobiera wszystkie pule przebiegu w przebiegu w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="12e42-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="12e42-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="12e42-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="12e42-114">To polecenie pobiera pulę przebiegu w przebiegu w obszarze roboczym ContosoWorkspace o nazwie ContosoSparkPool.</span><span class="sxs-lookup"><span data-stu-id="12e42-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="12e42-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="12e42-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="12e42-116">To polecenie pobiera wszystkie pule przebiegu w przebiegu w obszarze roboczym w ramach potoku.</span><span class="sxs-lookup"><span data-stu-id="12e42-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="12e42-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="12e42-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="12e42-118">To polecenie pobiera pulę przebiegu w czasie z określonym identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="12e42-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="12e42-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12e42-119">PARAMETERS</span></span>

### <span data-ttu-id="12e42-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e42-120">-DefaultProfile</span></span>
<span data-ttu-id="12e42-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="12e42-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e42-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="12e42-122">-Name</span></span>
<span data-ttu-id="12e42-123">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="12e42-123">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SparkPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e42-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e42-124">-ResourceGroupName</span></span>
<span data-ttu-id="12e42-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12e42-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e42-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12e42-126">-ResourceId</span></span>
<span data-ttu-id="12e42-127">Identyfikator zasobu puli synpsy przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="12e42-127">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e42-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="12e42-128">-WorkspaceName</span></span>
<span data-ttu-id="12e42-129">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="12e42-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e42-130">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="12e42-130">-WorkspaceObject</span></span>
<span data-ttu-id="12e42-131">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="12e42-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12e42-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e42-132">CommonParameters</span></span>
<span data-ttu-id="12e42-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e42-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e42-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12e42-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e42-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12e42-135">INPUTS</span></span>

### <span data-ttu-id="12e42-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="12e42-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="12e42-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="12e42-137">OUTPUTS</span></span>

### <span data-ttu-id="12e42-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="12e42-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="12e42-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="12e42-139">NOTES</span></span>

## <span data-ttu-id="12e42-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12e42-140">RELATED LINKS</span></span>
