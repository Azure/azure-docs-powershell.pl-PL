---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225640"
---
# <span data-ttu-id="b22b0-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="b22b0-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="b22b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b22b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b22b0-103">Tworzy nową grupę docelową</span><span class="sxs-lookup"><span data-stu-id="b22b0-103">Creates a new target group</span></span>

## <span data-ttu-id="b22b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b22b0-104">SYNTAX</span></span>

### <span data-ttu-id="b22b0-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b22b0-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b22b0-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="b22b0-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b22b0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b22b0-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b22b0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b22b0-108">DESCRIPTION</span></span>
<span data-ttu-id="b22b0-109">Polecenie cmdlet New-AzSqlElasticJobTargetGroup tworzy nową grupę docelową</span><span class="sxs-lookup"><span data-stu-id="b22b0-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="b22b0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b22b0-110">EXAMPLES</span></span>

### <span data-ttu-id="b22b0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b22b0-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="b22b0-112">Tworzenie pustej grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="b22b0-112">Creates an empty target group</span></span>

## <span data-ttu-id="b22b0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b22b0-113">PARAMETERS</span></span>

### <span data-ttu-id="b22b0-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b22b0-114">-AgentName</span></span>
<span data-ttu-id="b22b0-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="b22b0-115">The agent name</span></span>

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

### <span data-ttu-id="b22b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22b0-116">-DefaultProfile</span></span>
<span data-ttu-id="b22b0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b22b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b22b0-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b22b0-118">-Name</span></span>
<span data-ttu-id="b22b0-119">Nazwa grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="b22b0-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22b0-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="b22b0-120">-ParentObject</span></span>
<span data-ttu-id="b22b0-121">Obiekt wejściowy agenta</span><span class="sxs-lookup"><span data-stu-id="b22b0-121">The agent input object</span></span>

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

### <span data-ttu-id="b22b0-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b22b0-122">-ParentResourceId</span></span>
<span data-ttu-id="b22b0-123">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="b22b0-123">The agent resource id</span></span>

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

### <span data-ttu-id="b22b0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b22b0-124">-ResourceGroupName</span></span>
<span data-ttu-id="b22b0-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b22b0-125">The resource group name</span></span>

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

### <span data-ttu-id="b22b0-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b22b0-126">-ServerName</span></span>
<span data-ttu-id="b22b0-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="b22b0-127">The server name</span></span>

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

### <span data-ttu-id="b22b0-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b22b0-128">-Confirm</span></span>
<span data-ttu-id="b22b0-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b22b0-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22b0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b22b0-130">-WhatIf</span></span>
<span data-ttu-id="b22b0-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b22b0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b22b0-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b22b0-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22b0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22b0-133">CommonParameters</span></span>
<span data-ttu-id="b22b0-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b22b0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22b0-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b22b0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22b0-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b22b0-136">INPUTS</span></span>

### <span data-ttu-id="b22b0-137">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="b22b0-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="b22b0-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b22b0-138">OUTPUTS</span></span>

### <span data-ttu-id="b22b0-139">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="b22b0-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="b22b0-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b22b0-140">NOTES</span></span>

## <span data-ttu-id="b22b0-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b22b0-141">RELATED LINKS</span></span>
