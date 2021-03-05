---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 313748a0d674146ae0442174ee50a7069f55b9b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996773"
---
# <span data-ttu-id="1fe83-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="1fe83-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="1fe83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fe83-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe83-103">Usuwa wystąpienie usługi migracji bazy danych Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe83-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="1fe83-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1fe83-104">SYNTAX</span></span>

### <span data-ttu-id="1fe83-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1fe83-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fe83-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fe83-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fe83-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fe83-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fe83-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1fe83-108">DESCRIPTION</span></span>
<span data-ttu-id="1fe83-109">Polecenie Remove-AzDataMigrationService usuwa wystąpienie usługi migracji bazy danych Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe83-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="1fe83-110">Dostarczenie parametru DeleteRunningTask powoduje usunięcie wszystkich zadań usługi Azure Database Migration Service skojarzonych z usuwaną usługą.</span><span class="sxs-lookup"><span data-stu-id="1fe83-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="1fe83-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1fe83-111">EXAMPLES</span></span>

### <span data-ttu-id="1fe83-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1fe83-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="1fe83-113">W powyższym przykładzie usuniemy wystąpienie usługi migracji bazy danych Azure o nazwie TestService, które znajduje się w grupie zasobów platformy Azure o nazwie MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1fe83-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="1fe83-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fe83-114">PARAMETERS</span></span>

### <span data-ttu-id="1fe83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe83-115">-DefaultProfile</span></span>
<span data-ttu-id="1fe83-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe83-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fe83-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="1fe83-117">-DeleteRunningTask</span></span>
<span data-ttu-id="1fe83-118">Usuwanie dowolnego zadania uruchomionego</span><span class="sxs-lookup"><span data-stu-id="1fe83-118">Delete any running task</span></span>

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

### <span data-ttu-id="1fe83-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1fe83-119">-Force</span></span>
<span data-ttu-id="1fe83-120">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="1fe83-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1fe83-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fe83-121">-InputObject</span></span>
<span data-ttu-id="1fe83-122">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="1fe83-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe83-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1fe83-123">-Name</span></span>
<span data-ttu-id="1fe83-124">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1fe83-124">The name of the Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe83-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fe83-125">-PassThru</span></span>
<span data-ttu-id="1fe83-126">Zwraca wartość prawda/fałsz.</span><span class="sxs-lookup"><span data-stu-id="1fe83-126">Returns an true/false.</span></span>
<span data-ttu-id="1fe83-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1fe83-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1fe83-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe83-128">-ResourceGroupName</span></span>
<span data-ttu-id="1fe83-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1fe83-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="1fe83-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fe83-130">-ResourceId</span></span>
<span data-ttu-id="1fe83-131">Identyfikator zasobu usługi DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="1fe83-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="1fe83-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1fe83-132">-Confirm</span></span>
<span data-ttu-id="1fe83-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1fe83-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fe83-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe83-134">-WhatIf</span></span>
<span data-ttu-id="1fe83-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fe83-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fe83-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1fe83-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fe83-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe83-137">CommonParameters</span></span>
<span data-ttu-id="1fe83-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fe83-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe83-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe83-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe83-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fe83-140">INPUTS</span></span>

### <span data-ttu-id="1fe83-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="1fe83-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="1fe83-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1fe83-142">System.String</span></span>

## <span data-ttu-id="1fe83-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fe83-143">OUTPUTS</span></span>

### <span data-ttu-id="1fe83-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1fe83-144">System.Boolean</span></span>

## <span data-ttu-id="1fe83-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1fe83-145">NOTES</span></span>

## <span data-ttu-id="1fe83-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fe83-146">RELATED LINKS</span></span>
