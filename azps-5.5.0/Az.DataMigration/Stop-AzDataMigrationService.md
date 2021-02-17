---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: a4b4ec4f24f61e188a3ab8b9cf66e8e326142bd3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186146"
---
# <span data-ttu-id="fee5f-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="fee5f-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="fee5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fee5f-102">SYNOPSIS</span></span>
<span data-ttu-id="fee5f-103">Zatrzymuje wystąpienie usługi migracji bazy danych Azure, które znajduje się w stanie uruchomionym.</span><span class="sxs-lookup"><span data-stu-id="fee5f-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="fee5f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fee5f-104">SYNTAX</span></span>

### <span data-ttu-id="fee5f-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="fee5f-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fee5f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fee5f-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fee5f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fee5f-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fee5f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fee5f-108">DESCRIPTION</span></span>
<span data-ttu-id="fee5f-109">Polecenie Stop-AzDataMigrationService zatrzymuje wystąpienie usługi migracji bazy danych Azure, które znajduje się w stanie uruchomionym.</span><span class="sxs-lookup"><span data-stu-id="fee5f-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="fee5f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fee5f-110">EXAMPLES</span></span>

### <span data-ttu-id="fee5f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fee5f-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="fee5f-112">W powyższym przykładzie zatrzymano wystąpienie usługi migracji bazy danych Azure o nazwie TestService na podstawie nazwy usługi przekazanej jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="fee5f-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="fee5f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fee5f-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="fee5f-114">W powyższym przykładzie zatrzymane jest wystąpienie usługi migracji bazy danych Azure na podstawie obiektu PSDataMigrationService przekazywanego jako parametr wejściowy.</span><span class="sxs-lookup"><span data-stu-id="fee5f-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="fee5f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fee5f-115">PARAMETERS</span></span>

### <span data-ttu-id="fee5f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee5f-116">-DefaultProfile</span></span>
<span data-ttu-id="fee5f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fee5f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fee5f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fee5f-118">-InputObject</span></span>
<span data-ttu-id="fee5f-119">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="fee5f-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="fee5f-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fee5f-120">-Name</span></span>
<span data-ttu-id="fee5f-121">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fee5f-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="fee5f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fee5f-122">-PassThru</span></span>
<span data-ttu-id="fee5f-123">Zwraca wartość prawda/fałsz.</span><span class="sxs-lookup"><span data-stu-id="fee5f-123">Returns an true/false.</span></span>
<span data-ttu-id="fee5f-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fee5f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fee5f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee5f-125">-ResourceGroupName</span></span>
<span data-ttu-id="fee5f-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fee5f-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="fee5f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fee5f-127">-ResourceId</span></span>
<span data-ttu-id="fee5f-128">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="fee5f-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="fee5f-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fee5f-129">-Confirm</span></span>
<span data-ttu-id="fee5f-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fee5f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee5f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee5f-131">-WhatIf</span></span>
<span data-ttu-id="fee5f-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fee5f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fee5f-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fee5f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fee5f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee5f-134">CommonParameters</span></span>
<span data-ttu-id="fee5f-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee5f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee5f-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fee5f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee5f-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fee5f-137">INPUTS</span></span>

### <span data-ttu-id="fee5f-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="fee5f-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="fee5f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fee5f-139">System.String</span></span>

## <span data-ttu-id="fee5f-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fee5f-140">OUTPUTS</span></span>

### <span data-ttu-id="fee5f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fee5f-141">System.Boolean</span></span>

## <span data-ttu-id="fee5f-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fee5f-142">NOTES</span></span>

## <span data-ttu-id="fee5f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fee5f-143">RELATED LINKS</span></span>
