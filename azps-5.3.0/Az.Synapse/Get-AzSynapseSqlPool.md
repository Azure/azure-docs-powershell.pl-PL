---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: 8199b14cf7b41eb99bb17f1692e762a07e127f26
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383873"
---
# <span data-ttu-id="5644b-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5644b-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="5644b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5644b-102">SYNOPSIS</span></span>
<span data-ttu-id="5644b-103">Pobiera pulę SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5644b-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5644b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5644b-104">SYNTAX</span></span>

### <span data-ttu-id="5644b-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5644b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5644b-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5644b-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5644b-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5644b-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5644b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5644b-108">DESCRIPTION</span></span>
<span data-ttu-id="5644b-109">Polecenie cmdlet **Get-AzSynapseSqlPool** pobiera informacje o puli SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5644b-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5644b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5644b-110">EXAMPLES</span></span>

### <span data-ttu-id="5644b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5644b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="5644b-112">To polecenie pobiera wszystkie pule SQL w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="5644b-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="5644b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5644b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="5644b-114">To polecenie pobiera pulę SQL w obszarze roboczym ContosoWorkspace z nazwą ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="5644b-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="5644b-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5644b-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="5644b-116">To polecenie pobiera wszystkie pule SQL w obszarze roboczym za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="5644b-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="5644b-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="5644b-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="5644b-118">To polecenie pobiera pulę SQL z określonym IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="5644b-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="5644b-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5644b-119">PARAMETERS</span></span>

### <span data-ttu-id="5644b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5644b-120">-DefaultProfile</span></span>
<span data-ttu-id="5644b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5644b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5644b-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5644b-122">-Name</span></span>
<span data-ttu-id="5644b-123">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5644b-123">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="5644b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5644b-124">-ResourceGroupName</span></span>
<span data-ttu-id="5644b-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5644b-125">Resource group name.</span></span>

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

### <span data-ttu-id="5644b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5644b-126">-ResourceId</span></span>
<span data-ttu-id="5644b-127">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5644b-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="5644b-128">-Version</span><span class="sxs-lookup"><span data-stu-id="5644b-128">-Version</span></span>
<span data-ttu-id="5644b-129">[Ta funkcja jest w ograniczonym podglądzie, początkowo dostępna tylko w przypadku niektórych abonamentów.] Wersja puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5644b-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="5644b-130">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="5644b-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="5644b-131">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="5644b-131">-WorkspaceName</span></span>
<span data-ttu-id="5644b-132">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="5644b-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5644b-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="5644b-133">-WorkspaceObject</span></span>
<span data-ttu-id="5644b-134">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="5644b-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5644b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5644b-135">CommonParameters</span></span>
<span data-ttu-id="5644b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5644b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5644b-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5644b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5644b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5644b-138">INPUTS</span></span>

### <span data-ttu-id="5644b-139">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5644b-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5644b-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5644b-140">OUTPUTS</span></span>

### <span data-ttu-id="5644b-141">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5644b-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5644b-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5644b-142">NOTES</span></span>

## <span data-ttu-id="5644b-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5644b-143">RELATED LINKS</span></span>
