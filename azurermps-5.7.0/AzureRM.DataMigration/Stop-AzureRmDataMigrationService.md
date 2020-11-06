---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 9a3028e019d3873105df079b67652f2157137ce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554157"
---
# <span data-ttu-id="fe014-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="fe014-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="fe014-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe014-102">SYNOPSIS</span></span>
<span data-ttu-id="fe014-103">Zatrzymuje wystąpienie usługi migracji bazy danych platformy Azure, która jest w stanie uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="fe014-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe014-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe014-104">SYNTAX</span></span>

### <span data-ttu-id="fe014-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fe014-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fe014-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe014-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fe014-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe014-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="fe014-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fe014-108">DESCRIPTION</span></span>
<span data-ttu-id="fe014-109">Polecenie cmdlet Stop-AzureRmDataMigrationService zatrzymuje wystąpienie usługi migracji bazy danych platformy Azure, która jest w stanie uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="fe014-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="fe014-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe014-110">EXAMPLES</span></span>

### <span data-ttu-id="fe014-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fe014-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService

```
<span data-ttu-id="fe014-112">W powyższym przykładzie zatrzymano wystąpienie usługi migracji bazy danych platformy Azure o nazwie TestService na podstawie nazwy usługi przekazanej jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="fe014-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="fe014-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fe014-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService

```
<span data-ttu-id="fe014-114">W powyższym przykładzie zatrzymano wystąpienie usługi migracji bazy danych platformy Azure opartej na obiekcie PSDataMigrationService przekazanym jako parametr wejściowy.</span><span class="sxs-lookup"><span data-stu-id="fe014-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>



## <span data-ttu-id="fe014-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe014-115">PARAMETERS</span></span>

### <span data-ttu-id="fe014-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe014-116">-Confirm</span></span>
<span data-ttu-id="fe014-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe014-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe014-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe014-118">-DefaultProfile</span></span>
<span data-ttu-id="fe014-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe014-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe014-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fe014-120">-InputObject</span></span>
<span data-ttu-id="fe014-121">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="fe014-121">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe014-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fe014-122">-Name</span></span>
<span data-ttu-id="fe014-123">Nazwa usługi migracji danych.</span><span class="sxs-lookup"><span data-stu-id="fe014-123">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe014-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe014-124">-PassThru</span></span>
<span data-ttu-id="fe014-125">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="fe014-125">Returns an true/false.</span></span>
<span data-ttu-id="fe014-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fe014-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe014-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe014-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe014-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe014-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="fe014-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe014-129">-ResourceId</span></span>
<span data-ttu-id="fe014-130">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="fe014-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="fe014-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe014-131">-WhatIf</span></span>
<span data-ttu-id="fe014-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe014-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe014-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fe014-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="fe014-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe014-134">INPUTS</span></span>

### <span data-ttu-id="fe014-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="fe014-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="fe014-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fe014-136">System.String</span></span>


## <span data-ttu-id="fe014-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe014-137">OUTPUTS</span></span>

### <span data-ttu-id="fe014-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe014-138">System.Boolean</span></span>


## <span data-ttu-id="fe014-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe014-139">NOTES</span></span>

## <span data-ttu-id="fe014-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe014-140">RELATED LINKS</span></span>

