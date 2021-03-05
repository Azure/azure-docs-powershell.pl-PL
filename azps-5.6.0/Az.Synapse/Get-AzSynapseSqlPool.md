---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: 532246d6e672c4e1770802ab2a0fb01af03455b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015681"
---
# <span data-ttu-id="b9737-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b9737-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="b9737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9737-102">SYNOPSIS</span></span>
<span data-ttu-id="b9737-103">Pobiera pulę SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b9737-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b9737-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b9737-104">SYNTAX</span></span>

### <span data-ttu-id="b9737-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b9737-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9737-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9737-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9737-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9737-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9737-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b9737-108">DESCRIPTION</span></span>
<span data-ttu-id="b9737-109">Polecenie **cmdlet Get-AzSynapseSqlPool** pobiera informacje o puli sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b9737-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b9737-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b9737-110">EXAMPLES</span></span>

### <span data-ttu-id="b9737-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b9737-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b9737-112">To polecenie pobiera wszystkie pule sql w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="b9737-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="b9737-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b9737-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="b9737-114">To polecenie pobiera pulę sql w obszarze roboczym ContosoWorkspace o nazwie ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="b9737-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="b9737-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b9737-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="b9737-116">To polecenie pobiera wszystkie pule SQL w obszarze roboczym za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="b9737-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="b9737-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="b9737-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="b9737-118">To polecenie pobiera pulę SQL o określonym identyfikatorze zasobu.</span><span class="sxs-lookup"><span data-stu-id="b9737-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="b9737-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9737-119">PARAMETERS</span></span>

### <span data-ttu-id="b9737-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9737-120">-DefaultProfile</span></span>
<span data-ttu-id="b9737-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9737-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9737-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b9737-122">-Name</span></span>
<span data-ttu-id="b9737-123">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="b9737-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SqlPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9737-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9737-124">-ResourceGroupName</span></span>
<span data-ttu-id="b9737-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b9737-125">Resource group name.</span></span>

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

### <span data-ttu-id="b9737-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9737-126">-ResourceId</span></span>
<span data-ttu-id="b9737-127">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="b9737-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="b9737-128">— Wersja</span><span class="sxs-lookup"><span data-stu-id="b9737-128">-Version</span></span>
<span data-ttu-id="b9737-129">[Ta funkcja jest w ograniczonym podglądzie, początkowo dostępna tylko dla niektórych subskrypcji.] Wersja puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="b9737-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="b9737-130">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="b9737-130">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9737-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b9737-131">-WorkspaceName</span></span>
<span data-ttu-id="b9737-132">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="b9737-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b9737-133">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b9737-133">-WorkspaceObject</span></span>
<span data-ttu-id="b9737-134">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="b9737-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b9737-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9737-135">CommonParameters</span></span>
<span data-ttu-id="b9737-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9737-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9737-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9737-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9737-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9737-138">INPUTS</span></span>

### <span data-ttu-id="b9737-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b9737-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b9737-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9737-140">OUTPUTS</span></span>

### <span data-ttu-id="b9737-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b9737-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="b9737-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b9737-142">NOTES</span></span>

## <span data-ttu-id="b9737-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9737-143">RELATED LINKS</span></span>
