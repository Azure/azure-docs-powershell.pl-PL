---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: f45134cae9c77108aca4084470fd7f919fde02a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180850"
---
# <span data-ttu-id="b1bc8-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="b1bc8-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="b1bc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="b1bc8-103">Usuwa projekt usługi migracji bazy danych Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="b1bc8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b1bc8-104">SYNTAX</span></span>

### <span data-ttu-id="b1bc8-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b1bc8-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1bc8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1bc8-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1bc8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1bc8-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1bc8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b1bc8-108">DESCRIPTION</span></span>
<span data-ttu-id="b1bc8-109">Polecenie Remove-AzDataMigrationProject cmdlet usuwa projekt usługi migracji bazy danych Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="b1bc8-110">Dostarczenie parametru DeleteRunningTask powoduje usunięcie wszystkich zadań usługi migracji bazy danych Azure skojarzonych z usuwanym projektem.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="b1bc8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b1bc8-111">EXAMPLES</span></span>

### <span data-ttu-id="b1bc8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b1bc8-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="b1bc8-113">Powyższy przykład usuwa projekt usługi migracji bazy danych Azure o nazwie myDMProject z platformy Azure na podstawie nazwy jako parametru wejściowego</span><span class="sxs-lookup"><span data-stu-id="b1bc8-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="b1bc8-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b1bc8-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="b1bc8-115">W powyższym przykładzie jako parametr wejściowy jest usuwany projekt Usługi migracji bazy danych Azure oparty na obiekcie PSProject.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="b1bc8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1bc8-116">PARAMETERS</span></span>

### <span data-ttu-id="b1bc8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1bc8-117">-DefaultProfile</span></span>
<span data-ttu-id="b1bc8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1bc8-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="b1bc8-119">-DeleteRunningTask</span></span>
<span data-ttu-id="b1bc8-120">Usuwanie dowolnego zadania uruchomionego</span><span class="sxs-lookup"><span data-stu-id="b1bc8-120">Delete any running task</span></span>

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

### <span data-ttu-id="b1bc8-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b1bc8-121">-Force</span></span>
<span data-ttu-id="b1bc8-122">Pomiń komunikat z potwierdzeniem wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="b1bc8-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b1bc8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1bc8-123">-InputObject</span></span>
<span data-ttu-id="b1bc8-124">Obiekt PSProject.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-124">PSProject Object.</span></span>

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

### <span data-ttu-id="b1bc8-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b1bc8-125">-Name</span></span>
<span data-ttu-id="b1bc8-126">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1bc8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1bc8-127">-PassThru</span></span>
<span data-ttu-id="b1bc8-128">Zwraca wartość prawda/fałsz.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-128">Returns an true/false.</span></span>
<span data-ttu-id="b1bc8-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1bc8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1bc8-130">-ResourceGroupName</span></span>
<span data-ttu-id="b1bc8-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="b1bc8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1bc8-132">-ResourceId</span></span>
<span data-ttu-id="b1bc8-133">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="b1bc8-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b1bc8-134">-ServiceName</span></span>
<span data-ttu-id="b1bc8-135">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="b1bc8-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1bc8-136">-Confirm</span></span>
<span data-ttu-id="b1bc8-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1bc8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1bc8-138">-WhatIf</span></span>
<span data-ttu-id="b1bc8-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1bc8-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1bc8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1bc8-141">CommonParameters</span></span>
<span data-ttu-id="b1bc8-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1bc8-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1bc8-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1bc8-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1bc8-144">INPUTS</span></span>

### <span data-ttu-id="b1bc8-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="b1bc8-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="b1bc8-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b1bc8-146">System.String</span></span>

## <span data-ttu-id="b1bc8-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1bc8-147">OUTPUTS</span></span>

### <span data-ttu-id="b1bc8-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1bc8-148">System.Boolean</span></span>

## <span data-ttu-id="b1bc8-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b1bc8-149">NOTES</span></span>

## <span data-ttu-id="b1bc8-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1bc8-150">RELATED LINKS</span></span>
