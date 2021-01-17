---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335785"
---
# <span data-ttu-id="a052f-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="a052f-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="a052f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a052f-102">SYNOPSIS</span></span>
<span data-ttu-id="a052f-103">Pobieranie jednej lub większej liczby grup docelowych zadań</span><span class="sxs-lookup"><span data-stu-id="a052f-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="a052f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a052f-104">SYNTAX</span></span>

### <span data-ttu-id="a052f-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a052f-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a052f-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="a052f-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a052f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a052f-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a052f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a052f-108">DESCRIPTION</span></span>
<span data-ttu-id="a052f-109">Polecenie cmdlet Get-AzSqlElasticJobTargetGroup pobiera grupę docelową i jej elementy docelowe</span><span class="sxs-lookup"><span data-stu-id="a052f-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="a052f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a052f-110">EXAMPLES</span></span>

### <span data-ttu-id="a052f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a052f-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="a052f-112">Pobiera grupę docelową i jej elementy docelowe</span><span class="sxs-lookup"><span data-stu-id="a052f-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="a052f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a052f-113">PARAMETERS</span></span>

### <span data-ttu-id="a052f-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a052f-114">-AgentName</span></span>
<span data-ttu-id="a052f-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="a052f-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a052f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a052f-116">-DefaultProfile</span></span>
<span data-ttu-id="a052f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a052f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a052f-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a052f-118">-Name</span></span>
<span data-ttu-id="a052f-119">Nazwa grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="a052f-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a052f-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="a052f-120">-ParentObject</span></span>
<span data-ttu-id="a052f-121">Obiekt Agent</span><span class="sxs-lookup"><span data-stu-id="a052f-121">The agent object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a052f-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a052f-122">-ParentResourceId</span></span>
<span data-ttu-id="a052f-123">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="a052f-123">The agent resource id</span></span>

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

### <span data-ttu-id="a052f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a052f-124">-ResourceGroupName</span></span>
<span data-ttu-id="a052f-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a052f-125">The resource group name</span></span>

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

### <span data-ttu-id="a052f-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a052f-126">-ServerName</span></span>
<span data-ttu-id="a052f-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="a052f-127">The server name</span></span>

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

### <span data-ttu-id="a052f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a052f-128">CommonParameters</span></span>
<span data-ttu-id="a052f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a052f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a052f-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a052f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a052f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a052f-131">INPUTS</span></span>

### <span data-ttu-id="a052f-132">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="a052f-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a052f-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a052f-133">OUTPUTS</span></span>

### <span data-ttu-id="a052f-134">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="a052f-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="a052f-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a052f-135">NOTES</span></span>

## <span data-ttu-id="a052f-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a052f-136">RELATED LINKS</span></span>
