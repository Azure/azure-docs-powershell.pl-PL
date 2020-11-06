---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: 677e89dd0def314744e507c6e61c745f39a081bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552099"
---
# <span data-ttu-id="825ba-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="825ba-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="825ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="825ba-102">SYNOPSIS</span></span>
<span data-ttu-id="825ba-103">Usuwa wystąpienie usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="825ba-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="825ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="825ba-104">SYNTAX</span></span>

### <span data-ttu-id="825ba-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="825ba-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="825ba-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="825ba-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="825ba-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="825ba-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="825ba-108">Opis</span><span class="sxs-lookup"><span data-stu-id="825ba-108">DESCRIPTION</span></span>
<span data-ttu-id="825ba-109">Polecenie cmdlet Remove-AzureRmDataMigrationService powoduje usunięcie wystąpienia usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="825ba-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="825ba-110">Podanie parametru DeleteRunningTask powoduje usunięcie wszystkich zadań usługi migracji bazy danych platformy Azure skojarzonych z usuwaną usługą.</span><span class="sxs-lookup"><span data-stu-id="825ba-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="825ba-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="825ba-111">EXAMPLES</span></span>

### <span data-ttu-id="825ba-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="825ba-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="825ba-113">W powyższym przykładzie usunięto wystąpienie usługi migracji bazy danych platformy Azure o nazwie TestService, która jest uwzględniona w grupie zasobów platformy Azure o nazwie moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="825ba-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="825ba-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="825ba-114">PARAMETERS</span></span>

### <span data-ttu-id="825ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="825ba-115">-DefaultProfile</span></span>
<span data-ttu-id="825ba-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="825ba-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="825ba-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="825ba-117">-DeleteRunningTask</span></span>
<span data-ttu-id="825ba-118">Usuwanie uruchomionego zadania</span><span class="sxs-lookup"><span data-stu-id="825ba-118">Delete any running task</span></span>

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

### <span data-ttu-id="825ba-119">-Force</span><span class="sxs-lookup"><span data-stu-id="825ba-119">-Force</span></span>
<span data-ttu-id="825ba-120">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="825ba-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="825ba-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="825ba-121">-InputObject</span></span>
<span data-ttu-id="825ba-122">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="825ba-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="825ba-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="825ba-123">-Name</span></span>
<span data-ttu-id="825ba-124">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="825ba-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="825ba-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="825ba-125">-PassThru</span></span>
<span data-ttu-id="825ba-126">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="825ba-126">Returns an true/false.</span></span>
<span data-ttu-id="825ba-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="825ba-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="825ba-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="825ba-128">-ResourceGroupName</span></span>
<span data-ttu-id="825ba-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="825ba-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="825ba-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="825ba-130">-ResourceId</span></span>
<span data-ttu-id="825ba-131">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="825ba-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="825ba-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="825ba-132">-Confirm</span></span>
<span data-ttu-id="825ba-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="825ba-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="825ba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="825ba-134">-WhatIf</span></span>
<span data-ttu-id="825ba-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="825ba-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="825ba-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="825ba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="825ba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="825ba-137">CommonParameters</span></span>
<span data-ttu-id="825ba-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="825ba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="825ba-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="825ba-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="825ba-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="825ba-140">INPUTS</span></span>

### <span data-ttu-id="825ba-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="825ba-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="825ba-142">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="825ba-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="825ba-143">System. String</span><span class="sxs-lookup"><span data-stu-id="825ba-143">System.String</span></span>

## <span data-ttu-id="825ba-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="825ba-144">OUTPUTS</span></span>

### <span data-ttu-id="825ba-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="825ba-145">System.Boolean</span></span>

## <span data-ttu-id="825ba-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="825ba-146">NOTES</span></span>

## <span data-ttu-id="825ba-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="825ba-147">RELATED LINKS</span></span>
