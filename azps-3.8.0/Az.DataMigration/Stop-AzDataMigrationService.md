---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: a4b4ec4f24f61e188a3ab8b9cf66e8e326142bd3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053518"
---
# <span data-ttu-id="e8019-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e8019-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="e8019-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8019-102">SYNOPSIS</span></span>
<span data-ttu-id="e8019-103">Zatrzymuje wystąpienie usługi migracji bazy danych platformy Azure, która jest w stanie uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e8019-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="e8019-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8019-104">SYNTAX</span></span>

### <span data-ttu-id="e8019-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e8019-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8019-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8019-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8019-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8019-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8019-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e8019-108">DESCRIPTION</span></span>
<span data-ttu-id="e8019-109">Polecenie cmdlet Stop-AzDataMigrationService zatrzymuje wystąpienie usługi migracji bazy danych platformy Azure, która jest w stanie uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e8019-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="e8019-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8019-110">EXAMPLES</span></span>

### <span data-ttu-id="e8019-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8019-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="e8019-112">W powyższym przykładzie zatrzymano wystąpienie usługi migracji bazy danych platformy Azure o nazwie TestService na podstawie nazwy usługi przekazanej jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="e8019-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="e8019-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e8019-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="e8019-114">W powyższym przykładzie zatrzymano wystąpienie usługi migracji bazy danych platformy Azure opartej na obiekcie PSDataMigrationService przekazanym jako parametr wejściowy.</span><span class="sxs-lookup"><span data-stu-id="e8019-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="e8019-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8019-115">PARAMETERS</span></span>

### <span data-ttu-id="e8019-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8019-116">-DefaultProfile</span></span>
<span data-ttu-id="e8019-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8019-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8019-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e8019-118">-InputObject</span></span>
<span data-ttu-id="e8019-119">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="e8019-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="e8019-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8019-120">-Name</span></span>
<span data-ttu-id="e8019-121">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e8019-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="e8019-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8019-122">-PassThru</span></span>
<span data-ttu-id="e8019-123">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="e8019-123">Returns an true/false.</span></span>
<span data-ttu-id="e8019-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e8019-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e8019-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8019-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8019-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8019-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="e8019-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8019-127">-ResourceId</span></span>
<span data-ttu-id="e8019-128">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="e8019-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="e8019-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8019-129">-Confirm</span></span>
<span data-ttu-id="e8019-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8019-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8019-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8019-131">-WhatIf</span></span>
<span data-ttu-id="e8019-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8019-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8019-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8019-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8019-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8019-134">CommonParameters</span></span>
<span data-ttu-id="e8019-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8019-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8019-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8019-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8019-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8019-137">INPUTS</span></span>

### <span data-ttu-id="e8019-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e8019-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="e8019-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e8019-139">System.String</span></span>

## <span data-ttu-id="e8019-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8019-140">OUTPUTS</span></span>

### <span data-ttu-id="e8019-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8019-141">System.Boolean</span></span>

## <span data-ttu-id="e8019-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8019-142">NOTES</span></span>

## <span data-ttu-id="e8019-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8019-143">RELATED LINKS</span></span>
