---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 6ff5bdb6a3de7b1704ee41de0b6ff0b0f736ec5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014593"
---
# <span data-ttu-id="288a0-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="288a0-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="288a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="288a0-102">SYNOPSIS</span></span>
<span data-ttu-id="288a0-103">Otrzymuje agenta zadania elastycznego języka AZURE SQL</span><span class="sxs-lookup"><span data-stu-id="288a0-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="288a0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="288a0-104">SYNTAX</span></span>

### <span data-ttu-id="288a0-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="288a0-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="288a0-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="288a0-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="288a0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="288a0-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="288a0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="288a0-108">DESCRIPTION</span></span>
<span data-ttu-id="288a0-109">Polecenie Get-AzSqlElasticJobAgent cmdlet pobiera co najmniej jednego elastycznego agentów zadania</span><span class="sxs-lookup"><span data-stu-id="288a0-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="288a0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="288a0-110">EXAMPLES</span></span>

### <span data-ttu-id="288a0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="288a0-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="288a0-112">Otrzymuje elastycznego agenta zadania</span><span class="sxs-lookup"><span data-stu-id="288a0-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="288a0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="288a0-113">PARAMETERS</span></span>

### <span data-ttu-id="288a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="288a0-114">-DefaultProfile</span></span>
<span data-ttu-id="288a0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="288a0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="288a0-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="288a0-116">-Name</span></span>
<span data-ttu-id="288a0-117">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="288a0-117">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="288a0-118">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="288a0-118">-ParentObject</span></span>
<span data-ttu-id="288a0-119">Obiekt wejściowy serwera</span><span class="sxs-lookup"><span data-stu-id="288a0-119">The server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="288a0-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="288a0-120">-ParentResourceId</span></span>
<span data-ttu-id="288a0-121">Identyfikator zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="288a0-121">The server resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="288a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="288a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="288a0-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="288a0-123">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="288a0-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="288a0-124">-ServerName</span></span>
<span data-ttu-id="288a0-125">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="288a0-125">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="288a0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="288a0-126">CommonParameters</span></span>
<span data-ttu-id="288a0-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="288a0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="288a0-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="288a0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="288a0-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="288a0-129">INPUTS</span></span>

### <span data-ttu-id="288a0-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="288a0-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="288a0-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="288a0-131">OUTPUTS</span></span>

### <span data-ttu-id="288a0-132">Microsoft.Azure.Commands.sql.Jego elastycznaobs.model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="288a0-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="288a0-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="288a0-133">NOTES</span></span>

## <span data-ttu-id="288a0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="288a0-134">RELATED LINKS</span></span>
