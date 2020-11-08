---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: c203e9c80978f50bd7879627b733de2ec0c6cf7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225286"
---
# <span data-ttu-id="2b346-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b346-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="2b346-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b346-102">SYNOPSIS</span></span>
<span data-ttu-id="2b346-103">Pobiera bazę danych SQL analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="2b346-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="2b346-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b346-104">SYNTAX</span></span>

### <span data-ttu-id="2b346-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2b346-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b346-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b346-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b346-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b346-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b346-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2b346-108">DESCRIPTION</span></span>
<span data-ttu-id="2b346-109">[Ta funkcja jest w ograniczonym podglądzie, początkowo dostępna tylko w przypadku niektórych abonamentów.] Polecenie cmdlet **Get-AzSynapseSqlDatabase** pobiera informacje o bazie danych SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2b346-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="2b346-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b346-110">EXAMPLES</span></span>

### <span data-ttu-id="2b346-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2b346-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="2b346-112">To polecenie pobiera wszystkie bazy danych SQL w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="2b346-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="2b346-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2b346-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="2b346-114">To polecenie pobiera bazę danych SQL w obszarze roboczym ContosoWorkspace z nazwą ContosoSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="2b346-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="2b346-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2b346-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="2b346-116">To polecenie pobiera wszystkie bazy danych SQL w obszarze roboczym za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="2b346-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="2b346-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="2b346-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="2b346-118">To polecenie pobiera bazę danych SQL z określonym IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="2b346-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="2b346-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b346-119">PARAMETERS</span></span>

### <span data-ttu-id="2b346-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b346-120">-DefaultProfile</span></span>
<span data-ttu-id="2b346-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b346-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b346-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b346-122">-Name</span></span>
<span data-ttu-id="2b346-123">Nazwa bazy danych SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="2b346-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b346-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b346-124">-ResourceGroupName</span></span>
<span data-ttu-id="2b346-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2b346-125">Resource group name.</span></span>

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

### <span data-ttu-id="2b346-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b346-126">-ResourceId</span></span>
<span data-ttu-id="2b346-127">Identyfikator zasobu bazy danych SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="2b346-127">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="2b346-128">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="2b346-128">-WorkspaceName</span></span>
<span data-ttu-id="2b346-129">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="2b346-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2b346-130">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="2b346-130">-WorkspaceObject</span></span>
<span data-ttu-id="2b346-131">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="2b346-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2b346-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b346-132">CommonParameters</span></span>
<span data-ttu-id="2b346-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b346-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b346-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b346-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b346-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b346-135">INPUTS</span></span>

### <span data-ttu-id="2b346-136">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2b346-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2b346-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b346-137">OUTPUTS</span></span>

### <span data-ttu-id="2b346-138">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b346-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="2b346-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b346-139">NOTES</span></span>

## <span data-ttu-id="2b346-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b346-140">RELATED LINKS</span></span>
