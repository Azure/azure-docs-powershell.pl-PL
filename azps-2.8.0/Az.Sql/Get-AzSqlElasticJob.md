---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: 688926d05b56234ce11d4524afdcce326c5e09e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886977"
---
# <span data-ttu-id="c5faa-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="c5faa-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="c5faa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5faa-102">SYNOPSIS</span></span>
<span data-ttu-id="c5faa-103">Pobiera jeden lub więcej zadań</span><span class="sxs-lookup"><span data-stu-id="c5faa-103">Gets one or more jobs</span></span>

## <span data-ttu-id="c5faa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5faa-104">SYNTAX</span></span>

### <span data-ttu-id="c5faa-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c5faa-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5faa-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="c5faa-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5faa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c5faa-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5faa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c5faa-108">DESCRIPTION</span></span>
<span data-ttu-id="c5faa-109">Polecenie cmdlet Get-AzSqlElasticJob powoduje wyświetlenie jednego lub większej liczby zadań</span><span class="sxs-lookup"><span data-stu-id="c5faa-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="c5faa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5faa-110">EXAMPLES</span></span>

### <span data-ttu-id="c5faa-111">Przykład 1-pobiera zadanie</span><span class="sxs-lookup"><span data-stu-id="c5faa-111">Example 1 - Gets a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="c5faa-112">Pobiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="c5faa-112">Gets a job</span></span>

## <span data-ttu-id="c5faa-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5faa-113">PARAMETERS</span></span>

### <span data-ttu-id="c5faa-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c5faa-114">-AgentName</span></span>
<span data-ttu-id="c5faa-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="c5faa-115">The agent name</span></span>

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

### <span data-ttu-id="c5faa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5faa-116">-DefaultProfile</span></span>
<span data-ttu-id="c5faa-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5faa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5faa-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c5faa-118">-Name</span></span>
<span data-ttu-id="c5faa-119">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="c5faa-119">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5faa-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="c5faa-120">-ParentObject</span></span>
<span data-ttu-id="c5faa-121">Obiekt wejściowy agenta</span><span class="sxs-lookup"><span data-stu-id="c5faa-121">The agent input object</span></span>

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

### <span data-ttu-id="c5faa-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c5faa-122">-ParentResourceId</span></span>
<span data-ttu-id="c5faa-123">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="c5faa-123">The agent resource id</span></span>

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

### <span data-ttu-id="c5faa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5faa-124">-ResourceGroupName</span></span>
<span data-ttu-id="c5faa-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c5faa-125">The resource group name</span></span>

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

### <span data-ttu-id="c5faa-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c5faa-126">-ServerName</span></span>
<span data-ttu-id="c5faa-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="c5faa-127">The server name</span></span>

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

### <span data-ttu-id="c5faa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5faa-128">CommonParameters</span></span>
<span data-ttu-id="c5faa-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5faa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5faa-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5faa-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5faa-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5faa-131">INPUTS</span></span>

### <span data-ttu-id="c5faa-132">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="c5faa-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="c5faa-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5faa-133">OUTPUTS</span></span>

### <span data-ttu-id="c5faa-134">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="c5faa-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="c5faa-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5faa-135">NOTES</span></span>

## <span data-ttu-id="c5faa-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5faa-136">RELATED LINKS</span></span>
