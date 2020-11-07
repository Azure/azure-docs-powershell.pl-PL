---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 737f723fddd7b351a0f1e9189590a61d83454976
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705724"
---
# <span data-ttu-id="2449d-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2449d-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="2449d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2449d-102">SYNOPSIS</span></span>
<span data-ttu-id="2449d-103">Usuwa wystąpienie usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2449d-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="2449d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2449d-104">SYNTAX</span></span>

### <span data-ttu-id="2449d-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2449d-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2449d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2449d-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2449d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2449d-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2449d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2449d-108">DESCRIPTION</span></span>
<span data-ttu-id="2449d-109">Polecenie cmdlet Remove-AzDataMigrationService powoduje usunięcie wystąpienia usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2449d-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="2449d-110">Podanie parametru DeleteRunningTask powoduje usunięcie wszystkich zadań usługi migracji bazy danych platformy Azure skojarzonych z usuwaną usługą.</span><span class="sxs-lookup"><span data-stu-id="2449d-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="2449d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2449d-111">EXAMPLES</span></span>

### <span data-ttu-id="2449d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2449d-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="2449d-113">W powyższym przykładzie usunięto wystąpienie usługi migracji bazy danych platformy Azure o nazwie TestService, która jest uwzględniona w grupie zasobów platformy Azure o nazwie moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="2449d-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="2449d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2449d-114">PARAMETERS</span></span>

### <span data-ttu-id="2449d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2449d-115">-DefaultProfile</span></span>
<span data-ttu-id="2449d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2449d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2449d-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="2449d-117">-DeleteRunningTask</span></span>
<span data-ttu-id="2449d-118">Usuwanie uruchomionego zadania</span><span class="sxs-lookup"><span data-stu-id="2449d-118">Delete any running task</span></span>

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

### <span data-ttu-id="2449d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2449d-119">-Force</span></span>
<span data-ttu-id="2449d-120">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="2449d-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2449d-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2449d-121">-InputObject</span></span>
<span data-ttu-id="2449d-122">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="2449d-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="2449d-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2449d-123">-Name</span></span>
<span data-ttu-id="2449d-124">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2449d-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="2449d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2449d-125">-PassThru</span></span>
<span data-ttu-id="2449d-126">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="2449d-126">Returns an true/false.</span></span>
<span data-ttu-id="2449d-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2449d-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2449d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2449d-128">-ResourceGroupName</span></span>
<span data-ttu-id="2449d-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2449d-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="2449d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2449d-130">-ResourceId</span></span>
<span data-ttu-id="2449d-131">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="2449d-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="2449d-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2449d-132">-Confirm</span></span>
<span data-ttu-id="2449d-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2449d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2449d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2449d-134">-WhatIf</span></span>
<span data-ttu-id="2449d-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2449d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2449d-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2449d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2449d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2449d-137">CommonParameters</span></span>
<span data-ttu-id="2449d-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2449d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2449d-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2449d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2449d-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2449d-140">INPUTS</span></span>

### <span data-ttu-id="2449d-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2449d-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="2449d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2449d-142">System.String</span></span>

## <span data-ttu-id="2449d-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2449d-143">OUTPUTS</span></span>

### <span data-ttu-id="2449d-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2449d-144">System.Boolean</span></span>

## <span data-ttu-id="2449d-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2449d-145">NOTES</span></span>

## <span data-ttu-id="2449d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2449d-146">RELATED LINKS</span></span>
