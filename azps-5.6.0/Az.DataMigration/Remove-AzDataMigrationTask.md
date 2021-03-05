---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: acb7e9b453b94381f4f5a2a0edf49e32258809ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996759"
---
# <span data-ttu-id="da34a-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="da34a-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="da34a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da34a-102">SYNOPSIS</span></span>
<span data-ttu-id="da34a-103">Usuwa zadanie usługi migracji bazy danych Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="da34a-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="da34a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="da34a-104">SYNTAX</span></span>

### <span data-ttu-id="da34a-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="da34a-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da34a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da34a-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da34a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da34a-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da34a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="da34a-108">DESCRIPTION</span></span>
<span data-ttu-id="da34a-109">Polecenie Remove-AzDataMigrationTask usuwa zadanie usługi migracji bazy danych Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="da34a-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="da34a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="da34a-110">EXAMPLES</span></span>

### <span data-ttu-id="da34a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da34a-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="da34a-112">Poprzedni przykład usuwa zadanie usługi migracji bazy danych Azure o nazwie TestZadanie z platformy Azure na podstawie parametru nazwy zadania.</span><span class="sxs-lookup"><span data-stu-id="da34a-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="da34a-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="da34a-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="da34a-114">Poprzedni przykład usuwa zadanie usługi migracji bazy danych Azure na podstawie przekazanego obiektu PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="da34a-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="da34a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da34a-115">PARAMETERS</span></span>

### <span data-ttu-id="da34a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da34a-116">-DefaultProfile</span></span>
<span data-ttu-id="da34a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="da34a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da34a-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="da34a-118">-Force</span></span>
<span data-ttu-id="da34a-119">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="da34a-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="da34a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da34a-120">-InputObject</span></span>
<span data-ttu-id="da34a-121">Obiekt PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="da34a-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da34a-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="da34a-122">-Name</span></span>
<span data-ttu-id="da34a-123">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="da34a-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da34a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da34a-124">-PassThru</span></span>
<span data-ttu-id="da34a-125">Zwraca wartość prawda/fałsz.</span><span class="sxs-lookup"><span data-stu-id="da34a-125">Returns an true/false.</span></span>
<span data-ttu-id="da34a-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="da34a-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="da34a-127">— Nazwa_projektu</span><span class="sxs-lookup"><span data-stu-id="da34a-127">-ProjectName</span></span>
<span data-ttu-id="da34a-128">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="da34a-128">The name of the project.</span></span>

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

### <span data-ttu-id="da34a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da34a-129">-ResourceGroupName</span></span>
<span data-ttu-id="da34a-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="da34a-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="da34a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da34a-131">-ResourceId</span></span>
<span data-ttu-id="da34a-132">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="da34a-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="da34a-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="da34a-133">-ServiceName</span></span>
<span data-ttu-id="da34a-134">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="da34a-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="da34a-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da34a-135">-Confirm</span></span>
<span data-ttu-id="da34a-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="da34a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da34a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da34a-137">-WhatIf</span></span>
<span data-ttu-id="da34a-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da34a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da34a-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="da34a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da34a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da34a-140">CommonParameters</span></span>
<span data-ttu-id="da34a-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da34a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da34a-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da34a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da34a-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da34a-143">INPUTS</span></span>

### <span data-ttu-id="da34a-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="da34a-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="da34a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="da34a-145">System.String</span></span>

## <span data-ttu-id="da34a-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da34a-146">OUTPUTS</span></span>

### <span data-ttu-id="da34a-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="da34a-147">System.Boolean</span></span>

## <span data-ttu-id="da34a-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="da34a-148">NOTES</span></span>

## <span data-ttu-id="da34a-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da34a-149">RELATED LINKS</span></span>
