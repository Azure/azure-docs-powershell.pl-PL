---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: 8199b14cf7b41eb99bb17f1692e762a07e127f26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241714"
---
# <span data-ttu-id="79518-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="79518-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="79518-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79518-102">SYNOPSIS</span></span>
<span data-ttu-id="79518-103">Pobiera pulę SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="79518-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="79518-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79518-104">SYNTAX</span></span>

### <span data-ttu-id="79518-105">GetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="79518-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79518-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79518-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79518-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79518-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79518-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="79518-108">DESCRIPTION</span></span>
<span data-ttu-id="79518-109">Polecenie **cmdlet Get-AzSynapseSqlPool** pobiera informacje o puli sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="79518-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="79518-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79518-110">EXAMPLES</span></span>

### <span data-ttu-id="79518-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79518-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="79518-112">To polecenie pobiera wszystkie pule języka SQL w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="79518-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="79518-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="79518-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="79518-114">To polecenie pobiera pulę sql w obszarze roboczym ContosoWorkspace o nazwie ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="79518-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="79518-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="79518-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="79518-116">To polecenie pobiera wszystkie pule SQL w obszarze roboczym za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="79518-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="79518-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="79518-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="79518-118">To polecenie pobiera pulę SQL o określonym identyfikatorze zasobu.</span><span class="sxs-lookup"><span data-stu-id="79518-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="79518-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79518-119">PARAMETERS</span></span>

### <span data-ttu-id="79518-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79518-120">-DefaultProfile</span></span>
<span data-ttu-id="79518-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="79518-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79518-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="79518-122">-Name</span></span>
<span data-ttu-id="79518-123">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="79518-123">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="79518-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79518-124">-ResourceGroupName</span></span>
<span data-ttu-id="79518-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="79518-125">Resource group name.</span></span>

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

### <span data-ttu-id="79518-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79518-126">-ResourceId</span></span>
<span data-ttu-id="79518-127">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="79518-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="79518-128">— Wersja</span><span class="sxs-lookup"><span data-stu-id="79518-128">-Version</span></span>
<span data-ttu-id="79518-129">[Ta funkcja jest w ograniczonym podglądzie, początkowo dostępna tylko dla niektórych subskrypcji.] Wersja puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="79518-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="79518-130">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="79518-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="79518-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="79518-131">-WorkspaceName</span></span>
<span data-ttu-id="79518-132">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="79518-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="79518-133">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="79518-133">-WorkspaceObject</span></span>
<span data-ttu-id="79518-134">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="79518-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="79518-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79518-135">CommonParameters</span></span>
<span data-ttu-id="79518-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79518-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79518-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79518-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79518-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79518-138">INPUTS</span></span>

### <span data-ttu-id="79518-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="79518-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="79518-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="79518-140">OUTPUTS</span></span>

### <span data-ttu-id="79518-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="79518-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="79518-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79518-142">NOTES</span></span>

## <span data-ttu-id="79518-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79518-143">RELATED LINKS</span></span>
