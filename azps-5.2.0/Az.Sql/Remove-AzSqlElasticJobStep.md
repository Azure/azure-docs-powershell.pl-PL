---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: b097c95f45700afabd3317a1014641da061d410d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347617"
---
# <span data-ttu-id="6a007-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="6a007-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="6a007-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a007-102">SYNOPSIS</span></span>
<span data-ttu-id="6a007-103">Usuwa krok zadania</span><span class="sxs-lookup"><span data-stu-id="6a007-103">Removes the job step</span></span>

## <span data-ttu-id="6a007-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a007-104">SYNTAX</span></span>

### <span data-ttu-id="6a007-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6a007-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a007-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="6a007-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a007-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6a007-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a007-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6a007-108">DESCRIPTION</span></span>
<span data-ttu-id="6a007-109">Polecenie cmdlet Remove-AzSqlElasticJobStep usuwa etap zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="6a007-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="6a007-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a007-110">EXAMPLES</span></span>

### <span data-ttu-id="6a007-111">Przykład 1: usunięcie kroku zlecenia z zadania</span><span class="sxs-lookup"><span data-stu-id="6a007-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="6a007-112">Usuwanie kroku zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="6a007-112">Removes a job step from a job</span></span>

### <span data-ttu-id="6a007-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6a007-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="6a007-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a007-114">PARAMETERS</span></span>

### <span data-ttu-id="6a007-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6a007-115">-AgentName</span></span>
<span data-ttu-id="6a007-116">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="6a007-116">The agent name</span></span>

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

### <span data-ttu-id="6a007-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a007-117">-DefaultProfile</span></span>
<span data-ttu-id="6a007-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a007-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a007-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6a007-119">-InputObject</span></span>
<span data-ttu-id="6a007-120">Obiekt wejściowy kroku zadania</span><span class="sxs-lookup"><span data-stu-id="6a007-120">The job step input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a007-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="6a007-121">-JobName</span></span>
<span data-ttu-id="6a007-122">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="6a007-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a007-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6a007-123">-Name</span></span>
<span data-ttu-id="6a007-124">Nazwa etapu zadania</span><span class="sxs-lookup"><span data-stu-id="6a007-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a007-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a007-125">-ResourceGroupName</span></span>
<span data-ttu-id="6a007-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6a007-126">The resource group name</span></span>

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

### <span data-ttu-id="6a007-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a007-127">-ResourceId</span></span>
<span data-ttu-id="6a007-128">Identyfikator zasobu krok zadania</span><span class="sxs-lookup"><span data-stu-id="6a007-128">The job step resource id</span></span>

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

### <span data-ttu-id="6a007-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="6a007-129">-ServerName</span></span>
<span data-ttu-id="6a007-130">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="6a007-130">The server name</span></span>

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

### <span data-ttu-id="6a007-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a007-131">-Confirm</span></span>
<span data-ttu-id="6a007-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a007-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a007-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a007-133">-WhatIf</span></span>
<span data-ttu-id="6a007-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a007-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a007-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6a007-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a007-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a007-136">CommonParameters</span></span>
<span data-ttu-id="6a007-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a007-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a007-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a007-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a007-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a007-139">INPUTS</span></span>

### <span data-ttu-id="6a007-140">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="6a007-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="6a007-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a007-141">OUTPUTS</span></span>

### <span data-ttu-id="6a007-142">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="6a007-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="6a007-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a007-143">NOTES</span></span>

## <span data-ttu-id="6a007-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a007-144">RELATED LINKS</span></span>
