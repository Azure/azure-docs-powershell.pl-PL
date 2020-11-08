---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
ms.openlocfilehash: 03f2e9af6b7225fd7622c03347bdea87c63453c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052157"
---
# <span data-ttu-id="0d3f7-101">Remove-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="0d3f7-101">Remove-AzSqlElasticJob</span></span>

## <span data-ttu-id="0d3f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d3f7-102">SYNOPSIS</span></span>
<span data-ttu-id="0d3f7-103">Usuwa zadanie.</span><span class="sxs-lookup"><span data-stu-id="0d3f7-103">Removes a job</span></span>

## <span data-ttu-id="0d3f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d3f7-104">SYNTAX</span></span>

### <span data-ttu-id="0d3f7-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0d3f7-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d3f7-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="0d3f7-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d3f7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0d3f7-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJob [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d3f7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0d3f7-108">DESCRIPTION</span></span>
<span data-ttu-id="0d3f7-109">Polecenie cmdlet Remove-AzSqlElasticJob usuwa zadanie</span><span class="sxs-lookup"><span data-stu-id="0d3f7-109">The Remove-AzSqlElasticJob cmdlet removes a job</span></span>

## <span data-ttu-id="0d3f7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d3f7-110">EXAMPLES</span></span>

### <span data-ttu-id="0d3f7-111">Przykład 1-Usuwa zadanie</span><span class="sxs-lookup"><span data-stu-id="0d3f7-111">Example 1 - Removes a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="0d3f7-112">Usuwa zadanie.</span><span class="sxs-lookup"><span data-stu-id="0d3f7-112">Removes a job</span></span>

## <span data-ttu-id="0d3f7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d3f7-113">PARAMETERS</span></span>

### <span data-ttu-id="0d3f7-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="0d3f7-114">-AgentName</span></span>
<span data-ttu-id="0d3f7-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="0d3f7-115">The agent name</span></span>

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

### <span data-ttu-id="0d3f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d3f7-116">-DefaultProfile</span></span>
<span data-ttu-id="0d3f7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d3f7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d3f7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0d3f7-118">-Force</span></span>
<span data-ttu-id="0d3f7-119">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="0d3f7-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0d3f7-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d3f7-120">-InputObject</span></span>
<span data-ttu-id="0d3f7-121">Obiekt wejściowy zlecenia</span><span class="sxs-lookup"><span data-stu-id="0d3f7-121">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d3f7-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0d3f7-122">-Name</span></span>
<span data-ttu-id="0d3f7-123">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="0d3f7-123">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d3f7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d3f7-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d3f7-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0d3f7-125">The resource group name</span></span>

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

### <span data-ttu-id="0d3f7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d3f7-126">-ResourceId</span></span>
<span data-ttu-id="0d3f7-127">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="0d3f7-127">The agent resource id</span></span>

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

### <span data-ttu-id="0d3f7-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0d3f7-128">-ServerName</span></span>
<span data-ttu-id="0d3f7-129">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="0d3f7-129">The server name</span></span>

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

### <span data-ttu-id="0d3f7-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d3f7-130">-Confirm</span></span>
<span data-ttu-id="0d3f7-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d3f7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d3f7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d3f7-132">-WhatIf</span></span>
<span data-ttu-id="0d3f7-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d3f7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d3f7-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0d3f7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d3f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d3f7-135">CommonParameters</span></span>
<span data-ttu-id="0d3f7-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d3f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d3f7-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d3f7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d3f7-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d3f7-138">INPUTS</span></span>

### <span data-ttu-id="0d3f7-139">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="0d3f7-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="0d3f7-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d3f7-140">OUTPUTS</span></span>

### <span data-ttu-id="0d3f7-141">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="0d3f7-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="0d3f7-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d3f7-142">NOTES</span></span>

## <span data-ttu-id="0d3f7-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d3f7-143">RELATED LINKS</span></span>
