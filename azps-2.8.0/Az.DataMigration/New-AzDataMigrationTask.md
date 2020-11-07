---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: c40bd5761d7e0966e7d756a758f79bfb3592a2ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705725"
---
# <span data-ttu-id="a5128-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="a5128-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="a5128-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5128-102">SYNOPSIS</span></span>
<span data-ttu-id="a5128-103">Tworzy i rozpoczyna zadanie migracji danych w usłudze migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5128-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="a5128-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5128-104">SYNTAX</span></span>

### <span data-ttu-id="a5128-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a5128-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5128-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5128-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5128-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5128-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5128-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a5128-108">DESCRIPTION</span></span>
<span data-ttu-id="a5128-109">Polecenie cmdlet New-AzDataMigrationTask służy do tworzenia zadania migracji danych.</span><span class="sxs-lookup"><span data-stu-id="a5128-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="a5128-110">To polecenie cmdlet przyjmuje parametry dla modułu wyliczającego typ zadania, grupę zasobów platformy Azure, nazwę skojarzonej usługi migracji bazy danych platformy Azure i projektu jako dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="a5128-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="a5128-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5128-111">EXAMPLES</span></span>

### <span data-ttu-id="a5128-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5128-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="a5128-113">Ten przykładowy skrypt przedstawia sposób tworzenia nowego zadania migracji danych o nazwie MyMigrationTask w projekcie o nazwie myDMSProject i usługi o nazwie TestService.</span><span class="sxs-lookup"><span data-stu-id="a5128-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="a5128-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5128-114">PARAMETERS</span></span>

### <span data-ttu-id="a5128-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5128-115">-DefaultProfile</span></span>
<span data-ttu-id="a5128-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5128-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5128-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a5128-117">-InputObject</span></span>
<span data-ttu-id="a5128-118">Obiekt PSProject.</span><span class="sxs-lookup"><span data-stu-id="a5128-118">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5128-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5128-119">-Name</span></span>
<span data-ttu-id="a5128-120">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="a5128-120">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5128-121">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="a5128-121">-ProjectName</span></span>
<span data-ttu-id="a5128-122">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="a5128-122">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5128-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5128-123">-ResourceGroupName</span></span>
<span data-ttu-id="a5128-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a5128-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5128-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5128-125">-ResourceId</span></span>
<span data-ttu-id="a5128-126">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="a5128-126">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5128-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a5128-127">-ServiceName</span></span>
<span data-ttu-id="a5128-128">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a5128-128">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5128-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="a5128-129">-TaskType</span></span>
<span data-ttu-id="a5128-130">Typ zadania.</span><span class="sxs-lookup"><span data-stu-id="a5128-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync, ConnectToSourceMongoDb, ConnectToTargetMongoDb, MigrateMongoDb, ValidateMongoDbMigration, ConnectToTargetSqlDbMiSync, ValidateSqlServerSqlDbMiSync, MigrateSqlServerSqlDbMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5128-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="a5128-131">-MigrationValidation</span></span> 
<span data-ttu-id="a5128-132">Obiekt odpowiedzi na zadanie z użyciem rozmowy sprawdzającej, opcjonalnej, ale zalecanej.</span><span class="sxs-lookup"><span data-stu-id="a5128-132">Task response object by validation call, optional but recommended.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5128-133">-Czekaj</span><span class="sxs-lookup"><span data-stu-id="a5128-133">-Wait</span></span>
<span data-ttu-id="a5128-134">Określa, czy czekać na zakończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="a5128-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="a5128-135">Jeśli flaga jest ustawiona, sprawdza co określoną liczbę sekund, aż zadanie zostanie zakończone, i powróć do użytkownika właściwości zadania, w którym można sprawdzić dane wyjściowe lub błąd.</span><span class="sxs-lookup"><span data-stu-id="a5128-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5128-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5128-136">-Confirm</span></span>
<span data-ttu-id="a5128-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5128-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5128-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5128-138">-WhatIf</span></span>
<span data-ttu-id="a5128-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5128-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5128-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a5128-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5128-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5128-141">CommonParameters</span></span>
<span data-ttu-id="a5128-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5128-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5128-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5128-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5128-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5128-144">INPUTS</span></span>

### <span data-ttu-id="a5128-145">Microsoft. Azure. Commands. datamigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="a5128-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="a5128-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a5128-146">System.String</span></span>

## <span data-ttu-id="a5128-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5128-147">OUTPUTS</span></span>

### <span data-ttu-id="a5128-148">Microsoft. Azure. Commands. datamigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="a5128-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="a5128-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5128-149">NOTES</span></span>

## <span data-ttu-id="a5128-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5128-150">RELATED LINKS</span></span>
