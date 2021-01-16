---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 7d2985d2e5361f7594dbccac2e67c7c550c9b0a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346537"
---
# <span data-ttu-id="360f8-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="360f8-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="360f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="360f8-102">SYNOPSIS</span></span>
<span data-ttu-id="360f8-103">Pobiera elastycznego agenta zadań SQL Azure</span><span class="sxs-lookup"><span data-stu-id="360f8-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="360f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="360f8-104">SYNTAX</span></span>

### <span data-ttu-id="360f8-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="360f8-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="360f8-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="360f8-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="360f8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="360f8-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="360f8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="360f8-108">DESCRIPTION</span></span>
<span data-ttu-id="360f8-109">Polecenie cmdlet Get-AzSqlElasticJobAgent pobiera jednego lub więcej elastycznych agentów zadań</span><span class="sxs-lookup"><span data-stu-id="360f8-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="360f8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="360f8-110">EXAMPLES</span></span>

### <span data-ttu-id="360f8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="360f8-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="360f8-112">Uzyskuje elastyczny Agent zadań</span><span class="sxs-lookup"><span data-stu-id="360f8-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="360f8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="360f8-113">PARAMETERS</span></span>

### <span data-ttu-id="360f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="360f8-114">-DefaultProfile</span></span>
<span data-ttu-id="360f8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="360f8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="360f8-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="360f8-116">-Name</span></span>
<span data-ttu-id="360f8-117">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="360f8-117">The agent name</span></span>

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

### <span data-ttu-id="360f8-118">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="360f8-118">-ParentObject</span></span>
<span data-ttu-id="360f8-119">Obiekt wejściowy serwera</span><span class="sxs-lookup"><span data-stu-id="360f8-119">The server input object</span></span>

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

### <span data-ttu-id="360f8-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="360f8-120">-ParentResourceId</span></span>
<span data-ttu-id="360f8-121">Identyfikator zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="360f8-121">The server resource id</span></span>

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

### <span data-ttu-id="360f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="360f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="360f8-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="360f8-123">The resource group name</span></span>

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

### <span data-ttu-id="360f8-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="360f8-124">-ServerName</span></span>
<span data-ttu-id="360f8-125">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="360f8-125">The server name</span></span>

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

### <span data-ttu-id="360f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360f8-126">CommonParameters</span></span>
<span data-ttu-id="360f8-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="360f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360f8-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="360f8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360f8-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="360f8-129">INPUTS</span></span>

### <span data-ttu-id="360f8-130">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="360f8-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="360f8-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="360f8-131">OUTPUTS</span></span>

### <span data-ttu-id="360f8-132">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="360f8-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="360f8-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="360f8-133">NOTES</span></span>

## <span data-ttu-id="360f8-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="360f8-134">RELATED LINKS</span></span>
