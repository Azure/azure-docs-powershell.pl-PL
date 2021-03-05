---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: 9a6d2ba213054ea6b670205e84e3fd3893c59eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978561"
---
# <span data-ttu-id="e7206-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e7206-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="e7206-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7206-102">SYNOPSIS</span></span>
<span data-ttu-id="e7206-103">Zatrzymuje wystąpienie usługi migracji bazy danych Azure, które znajduje się w stanie uruchomionym.</span><span class="sxs-lookup"><span data-stu-id="e7206-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="e7206-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7206-104">SYNTAX</span></span>

### <span data-ttu-id="e7206-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e7206-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7206-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7206-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7206-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7206-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7206-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7206-108">DESCRIPTION</span></span>
<span data-ttu-id="e7206-109">Polecenie Stop-AzDataMigrationService zatrzymuje wystąpienie usługi migracji bazy danych Azure, które znajduje się w stanie uruchomionym.</span><span class="sxs-lookup"><span data-stu-id="e7206-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="e7206-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7206-110">EXAMPLES</span></span>

### <span data-ttu-id="e7206-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7206-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="e7206-112">W powyższym przykładzie zatrzymano wystąpienie usługi migracji bazy danych Azure o nazwie TestService na podstawie nazwy usługi przekazanej jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="e7206-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="e7206-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e7206-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="e7206-114">W powyższym przykładzie zatrzymane jest wystąpienie usługi migracji bazy danych Azure na podstawie obiektu PSDataMigrationService przekazywanego jako parametr wejściowy.</span><span class="sxs-lookup"><span data-stu-id="e7206-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="e7206-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7206-115">PARAMETERS</span></span>

### <span data-ttu-id="e7206-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7206-116">-DefaultProfile</span></span>
<span data-ttu-id="e7206-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7206-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7206-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7206-118">-InputObject</span></span>
<span data-ttu-id="e7206-119">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="e7206-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="e7206-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e7206-120">-Name</span></span>
<span data-ttu-id="e7206-121">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e7206-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="e7206-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7206-122">-PassThru</span></span>
<span data-ttu-id="e7206-123">Zwraca wartość prawda/fałsz.</span><span class="sxs-lookup"><span data-stu-id="e7206-123">Returns an true/false.</span></span>
<span data-ttu-id="e7206-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e7206-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e7206-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7206-125">-ResourceGroupName</span></span>
<span data-ttu-id="e7206-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7206-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="e7206-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7206-127">-ResourceId</span></span>
<span data-ttu-id="e7206-128">Identyfikator zasobu usługi DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="e7206-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="e7206-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7206-129">-Confirm</span></span>
<span data-ttu-id="e7206-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e7206-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7206-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7206-131">-WhatIf</span></span>
<span data-ttu-id="e7206-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7206-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7206-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e7206-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7206-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7206-134">CommonParameters</span></span>
<span data-ttu-id="e7206-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7206-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7206-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7206-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7206-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7206-137">INPUTS</span></span>

### <span data-ttu-id="e7206-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e7206-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="e7206-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e7206-139">System.String</span></span>

## <span data-ttu-id="e7206-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7206-140">OUTPUTS</span></span>

### <span data-ttu-id="e7206-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e7206-141">System.Boolean</span></span>

## <span data-ttu-id="e7206-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7206-142">NOTES</span></span>

## <span data-ttu-id="e7206-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7206-143">RELATED LINKS</span></span>
