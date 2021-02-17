---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 2ba182833fc1d4c59d9164b6db5d68bcd3c499f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180843"
---
# <span data-ttu-id="313e2-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="313e2-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="313e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="313e2-102">SYNOPSIS</span></span>
<span data-ttu-id="313e2-103">Usuwa wystąpienie usługi migracji bazy danych Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="313e2-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="313e2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="313e2-104">SYNTAX</span></span>

### <span data-ttu-id="313e2-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="313e2-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="313e2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="313e2-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="313e2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="313e2-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="313e2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="313e2-108">DESCRIPTION</span></span>
<span data-ttu-id="313e2-109">Polecenie Remove-AzDataMigrationService usuwa wystąpienie usługi migracji bazy danych Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="313e2-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="313e2-110">Dostarczenie parametru DeleteRunningTask powoduje usunięcie wszystkich zadań usługi migracji bazy danych Azure skojarzonych z usuwaną usługą.</span><span class="sxs-lookup"><span data-stu-id="313e2-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="313e2-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="313e2-111">EXAMPLES</span></span>

### <span data-ttu-id="313e2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="313e2-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="313e2-113">W powyższym przykładzie usuniemy wystąpienie usługi migracji bazy danych Azure o nazwie TestService, które znajduje się w grupie zasobów platformy Azure o nazwie MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="313e2-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="313e2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="313e2-114">PARAMETERS</span></span>

### <span data-ttu-id="313e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313e2-115">-DefaultProfile</span></span>
<span data-ttu-id="313e2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="313e2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="313e2-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="313e2-117">-DeleteRunningTask</span></span>
<span data-ttu-id="313e2-118">Usuwanie dowolnego zadania uruchomionego</span><span class="sxs-lookup"><span data-stu-id="313e2-118">Delete any running task</span></span>

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

### <span data-ttu-id="313e2-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="313e2-119">-Force</span></span>
<span data-ttu-id="313e2-120">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="313e2-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="313e2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="313e2-121">-InputObject</span></span>
<span data-ttu-id="313e2-122">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="313e2-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="313e2-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="313e2-123">-Name</span></span>
<span data-ttu-id="313e2-124">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="313e2-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="313e2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="313e2-125">-PassThru</span></span>
<span data-ttu-id="313e2-126">Zwraca wartość prawda/fałsz.</span><span class="sxs-lookup"><span data-stu-id="313e2-126">Returns an true/false.</span></span>
<span data-ttu-id="313e2-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="313e2-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="313e2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="313e2-128">-ResourceGroupName</span></span>
<span data-ttu-id="313e2-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="313e2-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="313e2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="313e2-130">-ResourceId</span></span>
<span data-ttu-id="313e2-131">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="313e2-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="313e2-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="313e2-132">-Confirm</span></span>
<span data-ttu-id="313e2-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="313e2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="313e2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="313e2-134">-WhatIf</span></span>
<span data-ttu-id="313e2-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="313e2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="313e2-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="313e2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="313e2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313e2-137">CommonParameters</span></span>
<span data-ttu-id="313e2-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="313e2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313e2-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="313e2-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313e2-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="313e2-140">INPUTS</span></span>

### <span data-ttu-id="313e2-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="313e2-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="313e2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="313e2-142">System.String</span></span>

## <span data-ttu-id="313e2-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="313e2-143">OUTPUTS</span></span>

### <span data-ttu-id="313e2-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="313e2-144">System.Boolean</span></span>

## <span data-ttu-id="313e2-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="313e2-145">NOTES</span></span>

## <span data-ttu-id="313e2-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="313e2-146">RELATED LINKS</span></span>
