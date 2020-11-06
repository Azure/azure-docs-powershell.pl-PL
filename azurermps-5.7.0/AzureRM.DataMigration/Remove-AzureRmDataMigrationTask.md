---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: d192b7f422557b4d4373f794e98cdb2556db3c63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548120"
---
# <span data-ttu-id="c4ff8-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="c4ff8-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="c4ff8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ff8-103">Usuwa zadanie usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4ff8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4ff8-104">SYNTAX</span></span>

### <span data-ttu-id="c4ff8-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c4ff8-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c4ff8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4ff8-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c4ff8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4ff8-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="c4ff8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c4ff8-108">DESCRIPTION</span></span>
<span data-ttu-id="c4ff8-109">Polecenie cmdlet Remove-AzureRmDataMigrationTask usuwa zadanie usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="c4ff8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4ff8-110">EXAMPLES</span></span>

### <span data-ttu-id="c4ff8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c4ff8-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup

```

<span data-ttu-id="c4ff8-112">W powyższym przykładzie usunięto zadanie usługi migracji bazy danych platformy Azure o nazwie TestTask z usługi Azure na podstawie parametru nazwy zadania.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="c4ff8-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c4ff8-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –InputObject $TestTask

```

<span data-ttu-id="c4ff8-114">W powyższym przykładzie zadanie usługi migracji bazy danych platformy Azure zostało usunięte na podstawie przekazanego obiektu PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="c4ff8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4ff8-115">PARAMETERS</span></span>

### <span data-ttu-id="c4ff8-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4ff8-116">-Confirm</span></span>
<span data-ttu-id="c4ff8-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4ff8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ff8-118">-DefaultProfile</span></span>
<span data-ttu-id="c4ff8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4ff8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c4ff8-120">-Force</span></span>
<span data-ttu-id="c4ff8-121">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="c4ff8-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ff8-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c4ff8-122">-InputObject</span></span>
<span data-ttu-id="c4ff8-123">Obiekt PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-123">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ff8-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4ff8-124">-Name</span></span>
<span data-ttu-id="c4ff8-125">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-125">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ff8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4ff8-126">-PassThru</span></span>
<span data-ttu-id="c4ff8-127">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-127">Returns an true/false.</span></span>
<span data-ttu-id="c4ff8-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ff8-129">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="c4ff8-129">-ProjectName</span></span>
<span data-ttu-id="c4ff8-130">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-130">The name of the project.</span></span>

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

### <span data-ttu-id="c4ff8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ff8-131">-ResourceGroupName</span></span>
<span data-ttu-id="c4ff8-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="c4ff8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4ff8-133">-ResourceId</span></span>
<span data-ttu-id="c4ff8-134">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-134">Project Resource Id.</span></span>

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

### <span data-ttu-id="c4ff8-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c4ff8-135">-ServiceName</span></span>
<span data-ttu-id="c4ff8-136">Nazwa usługi migracji danych.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-136">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="c4ff8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4ff8-137">-WhatIf</span></span>
<span data-ttu-id="c4ff8-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4ff8-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c4ff8-139">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="c4ff8-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4ff8-140">INPUTS</span></span>

### <span data-ttu-id="c4ff8-141">Microsoft. Azure. Commands. datamigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="c4ff8-141">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="c4ff8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c4ff8-142">System.String</span></span>


## <span data-ttu-id="c4ff8-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4ff8-143">OUTPUTS</span></span>

### <span data-ttu-id="c4ff8-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4ff8-144">System.Boolean</span></span>


## <span data-ttu-id="c4ff8-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4ff8-145">NOTES</span></span>

## <span data-ttu-id="c4ff8-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4ff8-146">RELATED LINKS</span></span>


