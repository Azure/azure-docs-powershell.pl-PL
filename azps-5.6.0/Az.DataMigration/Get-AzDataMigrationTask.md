---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: 08f87d40eec10f10b12f568cae8e899f5b7468d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964753"
---
# <span data-ttu-id="b7381-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="b7381-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="b7381-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7381-102">SYNOPSIS</span></span>
<span data-ttu-id="b7381-103">Pobiera obiekt PSProjectTask skojarzony z zadaniem migracji usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="b7381-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="b7381-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b7381-104">SYNTAX</span></span>

### <span data-ttu-id="b7381-105">ListByComponent (Default)</span><span class="sxs-lookup"><span data-stu-id="b7381-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7381-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="b7381-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7381-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="b7381-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7381-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="b7381-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7381-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7381-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7381-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7381-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7381-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="b7381-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7381-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="b7381-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7381-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="b7381-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7381-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="b7381-114">DESCRIPTION</span></span>
<span data-ttu-id="b7381-115">Polecenie Get-AzDataMigrationTask pobiera właściwości skojarzone z zadaniem migracji usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="b7381-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="b7381-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b7381-116">EXAMPLES</span></span>

### <span data-ttu-id="b7381-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b7381-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="b7381-118">W powyższym przykładzie pokazano użycie polecenia cmdlet Get-AzDataMigrationTask w celu pobrania właściwości skojarzonych z zadaniem migracji usługi migracji bazy danych Azure na podstawie nazwy zadania przekazanej jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="b7381-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="b7381-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b7381-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="b7381-120">W powyższym przykładzie pokazano użycie polecenia cmdlet Get-AzDataMigrationTask w celu pobrania wszystkich zadań migracji skojarzonych z obiektem PSProject przekazanym jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="b7381-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="b7381-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7381-121">PARAMETERS</span></span>

### <span data-ttu-id="b7381-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7381-122">-DefaultProfile</span></span>
<span data-ttu-id="b7381-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7381-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7381-124">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="b7381-124">-Expand</span></span>
<span data-ttu-id="b7381-125">Rozwijanie danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="b7381-125">Expand output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7381-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7381-126">-InputObject</span></span>
<span data-ttu-id="b7381-127">Obiekt PSProject.</span><span class="sxs-lookup"><span data-stu-id="b7381-127">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7381-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b7381-128">-Name</span></span>
<span data-ttu-id="b7381-129">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="b7381-129">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7381-130">— Nazwa_projektu</span><span class="sxs-lookup"><span data-stu-id="b7381-130">-ProjectName</span></span>
<span data-ttu-id="b7381-131">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="b7381-131">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7381-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7381-132">-ResourceGroupName</span></span>
<span data-ttu-id="b7381-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7381-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7381-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7381-134">-ResourceId</span></span>
<span data-ttu-id="b7381-135">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="b7381-135">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7381-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="b7381-136">-ResultType</span></span>
<span data-ttu-id="b7381-137">Rozwijanie danych wyjściowych danego typu wyników.</span><span class="sxs-lookup"><span data-stu-id="b7381-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput, Command

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7381-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b7381-138">-ServiceName</span></span>
<span data-ttu-id="b7381-139">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b7381-139">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7381-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="b7381-140">-TaskType</span></span>
<span data-ttu-id="b7381-141">Filtruj według typu Zadania.</span><span class="sxs-lookup"><span data-stu-id="b7381-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7381-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7381-142">CommonParameters</span></span>
<span data-ttu-id="b7381-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7381-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7381-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7381-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7381-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7381-145">INPUTS</span></span>

### <span data-ttu-id="b7381-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="b7381-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="b7381-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b7381-147">System.String</span></span>

## <span data-ttu-id="b7381-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7381-148">OUTPUTS</span></span>

### <span data-ttu-id="b7381-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="b7381-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="b7381-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b7381-150">NOTES</span></span>

## <span data-ttu-id="b7381-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7381-151">RELATED LINKS</span></span>
