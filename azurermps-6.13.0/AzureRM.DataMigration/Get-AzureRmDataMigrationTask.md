---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: caab43824c63e73e7011c0377d0bd7665befe5dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548700"
---
# <span data-ttu-id="48bb6-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="48bb6-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="48bb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="48bb6-103">Pobiera obiekt PSProjectTask skojarzony z zadaniem migracji usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48bb6-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48bb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48bb6-104">SYNTAX</span></span>

### <span data-ttu-id="48bb6-105">ListByComponent (domyślny)</span><span class="sxs-lookup"><span data-stu-id="48bb6-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48bb6-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="48bb6-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48bb6-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="48bb6-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48bb6-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="48bb6-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48bb6-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="48bb6-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48bb6-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="48bb6-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48bb6-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="48bb6-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48bb6-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="48bb6-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48bb6-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="48bb6-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48bb6-114">Opis</span><span class="sxs-lookup"><span data-stu-id="48bb6-114">DESCRIPTION</span></span>
<span data-ttu-id="48bb6-115">Polecenie cmdlet Get-AzureRmDataMigrationTask pobiera właściwości skojarzone z zadaniem migracji usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48bb6-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="48bb6-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48bb6-116">EXAMPLES</span></span>

### <span data-ttu-id="48bb6-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="48bb6-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="48bb6-118">Powyższy przykład ilustruje użycie polecenia cmdlet Get-AzureRmDataMigrationTask w celu pobrania właściwości skojarzonych z zadaniem migracji usługi migracji bazy danych platformy Azure opartym na nazwie zadania przekazanej jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="48bb6-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="48bb6-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="48bb6-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="48bb6-120">Powyższy przykład ilustruje użycie polecenia cmdlet Get-AzureRmDataMigrationTask w celu pobrania wszystkich zadań migracji skojarzonych z obiektem PSProject przekazanym jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="48bb6-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="48bb6-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48bb6-121">PARAMETERS</span></span>

### <span data-ttu-id="48bb6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48bb6-122">-DefaultProfile</span></span>
<span data-ttu-id="48bb6-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48bb6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48bb6-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="48bb6-124">-Expand</span></span>
<span data-ttu-id="48bb6-125">Rozwijanie danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="48bb6-125">Expand output</span></span>

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

### <span data-ttu-id="48bb6-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="48bb6-126">-InputObject</span></span>
<span data-ttu-id="48bb6-127">Obiekt PSProject.</span><span class="sxs-lookup"><span data-stu-id="48bb6-127">PSProject Object.</span></span>

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

### <span data-ttu-id="48bb6-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48bb6-128">-Name</span></span>
<span data-ttu-id="48bb6-129">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="48bb6-129">The name of the task.</span></span>

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

### <span data-ttu-id="48bb6-130">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="48bb6-130">-ProjectName</span></span>
<span data-ttu-id="48bb6-131">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="48bb6-131">The name of the project.</span></span>

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

### <span data-ttu-id="48bb6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48bb6-132">-ResourceGroupName</span></span>
<span data-ttu-id="48bb6-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="48bb6-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="48bb6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48bb6-134">-ResourceId</span></span>
<span data-ttu-id="48bb6-135">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="48bb6-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="48bb6-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="48bb6-136">-ResultType</span></span>
<span data-ttu-id="48bb6-137">Rozwijanie danych wyjściowych danego typu wyników.</span><span class="sxs-lookup"><span data-stu-id="48bb6-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48bb6-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="48bb6-138">-ServiceName</span></span>
<span data-ttu-id="48bb6-139">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="48bb6-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="48bb6-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="48bb6-140">-TaskType</span></span>
<span data-ttu-id="48bb6-141">Filtrowanie wedługtype zadania.</span><span class="sxs-lookup"><span data-stu-id="48bb6-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48bb6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48bb6-142">CommonParameters</span></span>
<span data-ttu-id="48bb6-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48bb6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48bb6-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48bb6-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48bb6-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48bb6-145">INPUTS</span></span>

### <span data-ttu-id="48bb6-146">Microsoft. Azure. Commands. datamigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="48bb6-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="48bb6-147">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="48bb6-147">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="48bb6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="48bb6-148">System.String</span></span>

## <span data-ttu-id="48bb6-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48bb6-149">OUTPUTS</span></span>

### <span data-ttu-id="48bb6-150">Microsoft. Azure. Commands. datamigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="48bb6-150">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="48bb6-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48bb6-151">NOTES</span></span>

## <span data-ttu-id="48bb6-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48bb6-152">RELATED LINKS</span></span>
