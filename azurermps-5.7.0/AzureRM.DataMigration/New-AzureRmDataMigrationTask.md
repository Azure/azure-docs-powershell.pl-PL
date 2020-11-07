---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 1bdf66311acd1b8ff1de43b5ea199d5d0a17c394
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717119"
---
# <span data-ttu-id="02dca-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="02dca-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="02dca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02dca-102">SYNOPSIS</span></span>
<span data-ttu-id="02dca-103">Tworzy i rozpoczyna zadanie migracji danych w usłudze migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="02dca-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02dca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02dca-104">SYNTAX</span></span>

### <span data-ttu-id="02dca-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="02dca-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="02dca-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02dca-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="02dca-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02dca-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="02dca-108">Opis</span><span class="sxs-lookup"><span data-stu-id="02dca-108">DESCRIPTION</span></span>
<span data-ttu-id="02dca-109">Polecenie cmdlet New-AzureRmDataMigrationTask służy do tworzenia zadania migracji danych.</span><span class="sxs-lookup"><span data-stu-id="02dca-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="02dca-110">To polecenie cmdlet przyjmuje Parametry modułu wyliczającego typ zadania, grupę zasobów platformy Azure, nazwę skojarzonej usługi migracji danych platformy Azure i projektu jako dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="02dca-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Data Migration Service and Project as input.</span></span> 

## <span data-ttu-id="02dca-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02dca-111">EXAMPLES</span></span>

### <span data-ttu-id="02dca-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="02dca-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```
<span data-ttu-id="02dca-113">Ten przykładowy skrypt przedstawia sposób tworzenia nowego zadania migracji danych o nazwie MyMigrationTask w projekcie o nazwie myDMSProject i usługi o nazwie TestService.</span><span class="sxs-lookup"><span data-stu-id="02dca-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="02dca-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02dca-114">PARAMETERS</span></span>

### <span data-ttu-id="02dca-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02dca-115">-Confirm</span></span>
<span data-ttu-id="02dca-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02dca-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02dca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02dca-117">-DefaultProfile</span></span>
<span data-ttu-id="02dca-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02dca-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02dca-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="02dca-119">-InputObject</span></span>
<span data-ttu-id="02dca-120">Obiekt PSProject.</span><span class="sxs-lookup"><span data-stu-id="02dca-120">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02dca-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02dca-121">-Name</span></span>
<span data-ttu-id="02dca-122">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="02dca-122">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02dca-123">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="02dca-123">-ProjectName</span></span>
<span data-ttu-id="02dca-124">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="02dca-124">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02dca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02dca-125">-ResourceGroupName</span></span>
<span data-ttu-id="02dca-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="02dca-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02dca-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02dca-127">-ResourceId</span></span>
<span data-ttu-id="02dca-128">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="02dca-128">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02dca-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="02dca-129">-ServiceName</span></span>
<span data-ttu-id="02dca-130">Nazwa usługi migracji danych.</span><span class="sxs-lookup"><span data-stu-id="02dca-130">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02dca-131">-TaskType</span><span class="sxs-lookup"><span data-stu-id="02dca-131">-TaskType</span></span>
<span data-ttu-id="02dca-132">Typ zadania.</span><span class="sxs-lookup"><span data-stu-id="02dca-132">Task Type.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02dca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02dca-133">-WhatIf</span></span>
<span data-ttu-id="02dca-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02dca-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02dca-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02dca-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="02dca-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02dca-136">INPUTS</span></span>

### <span data-ttu-id="02dca-137">Microsoft. Azure. Commands. datamigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="02dca-137">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="02dca-138">System. String</span><span class="sxs-lookup"><span data-stu-id="02dca-138">System.String</span></span>


## <span data-ttu-id="02dca-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02dca-139">OUTPUTS</span></span>

### <span data-ttu-id="02dca-140">Microsoft. Azure. Commands. datamigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="02dca-140">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>


## <span data-ttu-id="02dca-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02dca-141">NOTES</span></span>

## <span data-ttu-id="02dca-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02dca-142">RELATED LINKS</span></span>


