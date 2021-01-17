---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359480"
---
# <span data-ttu-id="edd92-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="edd92-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="edd92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="edd92-102">SYNOPSIS</span></span>
<span data-ttu-id="edd92-103">Pobiera pulę Synapse analizy Spark.</span><span class="sxs-lookup"><span data-stu-id="edd92-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="edd92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="edd92-104">SYNTAX</span></span>

### <span data-ttu-id="edd92-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="edd92-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edd92-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="edd92-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edd92-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="edd92-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edd92-108">Opis</span><span class="sxs-lookup"><span data-stu-id="edd92-108">DESCRIPTION</span></span>
<span data-ttu-id="edd92-109">Polecenie cmdlet **Get-AzSynapseSparkPool** pobiera informacje o puli platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="edd92-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="edd92-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="edd92-110">EXAMPLES</span></span>

### <span data-ttu-id="edd92-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="edd92-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="edd92-112">To polecenie pobiera wszystkie pule Spark w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="edd92-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="edd92-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="edd92-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="edd92-114">To polecenie pobiera pulę platformy Spark w obszarze roboczym ContosoWorkspace z nazwą ContosoSparkPool.</span><span class="sxs-lookup"><span data-stu-id="edd92-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="edd92-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="edd92-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="edd92-116">To polecenie pobiera wszystkie pule usługi Spark w obszarze roboczym za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="edd92-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="edd92-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="edd92-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="edd92-118">To polecenie pobiera pulę Spark o określonym IDENTYFIKATORze zasobu.</span><span class="sxs-lookup"><span data-stu-id="edd92-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="edd92-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="edd92-119">PARAMETERS</span></span>

### <span data-ttu-id="edd92-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd92-120">-DefaultProfile</span></span>
<span data-ttu-id="edd92-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="edd92-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edd92-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="edd92-122">-Name</span></span>
<span data-ttu-id="edd92-123">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="edd92-123">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="edd92-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edd92-124">-ResourceGroupName</span></span>
<span data-ttu-id="edd92-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="edd92-125">Resource group name.</span></span>

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

### <span data-ttu-id="edd92-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edd92-126">-ResourceId</span></span>
<span data-ttu-id="edd92-127">Identyfikator zasobu puli usługi Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="edd92-127">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="edd92-128">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="edd92-128">-WorkspaceName</span></span>
<span data-ttu-id="edd92-129">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="edd92-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="edd92-130">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="edd92-130">-WorkspaceObject</span></span>
<span data-ttu-id="edd92-131">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="edd92-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="edd92-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd92-132">CommonParameters</span></span>
<span data-ttu-id="edd92-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edd92-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd92-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edd92-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd92-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edd92-135">INPUTS</span></span>

### <span data-ttu-id="edd92-136">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="edd92-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="edd92-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="edd92-137">OUTPUTS</span></span>

### <span data-ttu-id="edd92-138">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="edd92-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="edd92-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="edd92-139">NOTES</span></span>

## <span data-ttu-id="edd92-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edd92-140">RELATED LINKS</span></span>
