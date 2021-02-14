---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: 80d615f5a2a26869d748f652feeaa8909aca30d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188738"
---
# <span data-ttu-id="860d9-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="860d9-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="860d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="860d9-102">SYNOPSIS</span></span>
<span data-ttu-id="860d9-103">Sprawdza, czy istnieje pula języka SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="860d9-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="860d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="860d9-104">SYNTAX</span></span>

### <span data-ttu-id="860d9-105">TestByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="860d9-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="860d9-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="860d9-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="860d9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="860d9-107">DESCRIPTION</span></span>
<span data-ttu-id="860d9-108">Polecenie **cmdlet Test-AzSynapseSqlPool** sprawdza, czy istnieje pula SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="860d9-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="860d9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="860d9-109">EXAMPLES</span></span>

### <span data-ttu-id="860d9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="860d9-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="860d9-111">To polecenie sprawdza istnienie określonej puli sql.</span><span class="sxs-lookup"><span data-stu-id="860d9-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="860d9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="860d9-112">PARAMETERS</span></span>

### <span data-ttu-id="860d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860d9-113">-DefaultProfile</span></span>
<span data-ttu-id="860d9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="860d9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="860d9-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="860d9-115">-Name</span></span>
<span data-ttu-id="860d9-116">Nazwa puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="860d9-116">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860d9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="860d9-117">-ResourceGroupName</span></span>
<span data-ttu-id="860d9-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="860d9-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860d9-119">— Wersja</span><span class="sxs-lookup"><span data-stu-id="860d9-119">-Version</span></span>
<span data-ttu-id="860d9-120">Wersja puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="860d9-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="860d9-121">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="860d9-121">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="860d9-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="860d9-122">-WorkspaceName</span></span>
<span data-ttu-id="860d9-123">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="860d9-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860d9-124">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="860d9-124">-WorkspaceObject</span></span>
<span data-ttu-id="860d9-125">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="860d9-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="860d9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860d9-126">CommonParameters</span></span>
<span data-ttu-id="860d9-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="860d9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860d9-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="860d9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860d9-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="860d9-129">INPUTS</span></span>

### <span data-ttu-id="860d9-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="860d9-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="860d9-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="860d9-131">OUTPUTS</span></span>

### <span data-ttu-id="860d9-132">System.Object</span><span class="sxs-lookup"><span data-stu-id="860d9-132">System.Object</span></span>
## <span data-ttu-id="860d9-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="860d9-133">NOTES</span></span>

## <span data-ttu-id="860d9-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="860d9-134">RELATED LINKS</span></span>
