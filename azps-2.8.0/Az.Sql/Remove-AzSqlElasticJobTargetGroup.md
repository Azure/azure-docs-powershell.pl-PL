---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 4652774b07ca3ae58baf29b614bd63519d537a0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887329"
---
# <span data-ttu-id="f0b74-101">Remove-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="f0b74-101">Remove-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="f0b74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0b74-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b74-103">Usuwa grupę docelową.</span><span class="sxs-lookup"><span data-stu-id="f0b74-103">Removes the target group</span></span>

## <span data-ttu-id="f0b74-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0b74-104">SYNTAX</span></span>

### <span data-ttu-id="f0b74-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f0b74-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0b74-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="f0b74-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-InputObject] <AzureSqlElasticJobTargetGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0b74-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f0b74-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0b74-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f0b74-108">DESCRIPTION</span></span>
<span data-ttu-id="f0b74-109">Polecenie cmdlet Remove-AzSqlElasticJobTargetGroup powoduje usunięcie grupy docelowej i jej elementów docelowych.</span><span class="sxs-lookup"><span data-stu-id="f0b74-109">The Remove-AzSqlElasticJobTargetGroup cmdlet removes a target group and it's targets</span></span>

## <span data-ttu-id="f0b74-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0b74-110">EXAMPLES</span></span>

### <span data-ttu-id="f0b74-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f0b74-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent 
$agent | Remove-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="f0b74-112">Usuwanie grupy docelowej i jej elementów docelowych</span><span class="sxs-lookup"><span data-stu-id="f0b74-112">Removes a target group and it's targets</span></span>

## <span data-ttu-id="f0b74-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0b74-113">PARAMETERS</span></span>

### <span data-ttu-id="f0b74-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f0b74-114">-AgentName</span></span>
<span data-ttu-id="f0b74-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="f0b74-115">The agent name</span></span>

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

### <span data-ttu-id="f0b74-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b74-116">-DefaultProfile</span></span>
<span data-ttu-id="f0b74-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b74-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0b74-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f0b74-118">-Force</span></span>
<span data-ttu-id="f0b74-119">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="f0b74-119">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b74-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f0b74-120">-InputObject</span></span>
<span data-ttu-id="f0b74-121">Obiekt Grupa docelowa</span><span class="sxs-lookup"><span data-stu-id="f0b74-121">The target group object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b74-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f0b74-122">-Name</span></span>
<span data-ttu-id="f0b74-123">Nazwa grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="f0b74-123">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b74-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0b74-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0b74-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f0b74-125">The resource group name</span></span>

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

### <span data-ttu-id="f0b74-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0b74-126">-ResourceId</span></span>
<span data-ttu-id="f0b74-127">Identyfikator zasobu grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="f0b74-127">The target group resource id</span></span>

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

### <span data-ttu-id="f0b74-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f0b74-128">-ServerName</span></span>
<span data-ttu-id="f0b74-129">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="f0b74-129">The server name</span></span>

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

### <span data-ttu-id="f0b74-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0b74-130">-Confirm</span></span>
<span data-ttu-id="f0b74-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0b74-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0b74-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0b74-132">-WhatIf</span></span>
<span data-ttu-id="f0b74-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0b74-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0b74-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f0b74-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0b74-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b74-135">CommonParameters</span></span>
<span data-ttu-id="f0b74-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0b74-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b74-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0b74-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b74-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0b74-138">INPUTS</span></span>

### <span data-ttu-id="f0b74-139">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="f0b74-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="f0b74-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0b74-140">OUTPUTS</span></span>

### <span data-ttu-id="f0b74-141">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="f0b74-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="f0b74-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0b74-142">NOTES</span></span>

## <span data-ttu-id="f0b74-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0b74-143">RELATED LINKS</span></span>
