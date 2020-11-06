---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/start-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: 03f07eaac1dbf616c78d1ca39561945b2a844b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525133"
---
# <span data-ttu-id="8cb6c-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8cb6c-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="8cb6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8cb6c-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb6c-103">Powoduje uruchomienie wystąpienia usługi migracji bazy danych platformy Azure w stanie zatrzymanym.</span><span class="sxs-lookup"><span data-stu-id="8cb6c-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cb6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8cb6c-104">SYNTAX</span></span>

### <span data-ttu-id="8cb6c-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8cb6c-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8cb6c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cb6c-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8cb6c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cb6c-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8cb6c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8cb6c-108">DESCRIPTION</span></span>
<span data-ttu-id="8cb6c-109">Polecenie cmdlet Start-AzureRmDataMigrationService uruchamia wystąpienie usługi migracji bazy danych platformy Azure w stanie zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="8cb6c-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="8cb6c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8cb6c-110">EXAMPLES</span></span>

### <span data-ttu-id="8cb6c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8cb6c-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="8cb6c-112">W powyższym przykładzie rozpoczęto wystąpienie usługi migracji bazy danych platformy Azure o nazwie usługa testowa w stanie zatrzymania na podstawie nazwy usługi przekazanej jako dane wejściowe</span><span class="sxs-lookup"><span data-stu-id="8cb6c-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="8cb6c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8cb6c-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="8cb6c-114">W powyższym przykładzie rozpoczęto wystąpienie usługi migracji bazy danych platformy Azure na podstawie PSDataMigrationService przekazana jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="8cb6c-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="8cb6c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8cb6c-115">PARAMETERS</span></span>

### <span data-ttu-id="8cb6c-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8cb6c-116">-Confirm</span></span>
<span data-ttu-id="8cb6c-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cb6c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cb6c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb6c-118">-DefaultProfile</span></span>
<span data-ttu-id="8cb6c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8cb6c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cb6c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8cb6c-120">-InputObject</span></span>
<span data-ttu-id="8cb6c-121">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="8cb6c-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="8cb6c-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8cb6c-122">-Name</span></span>
<span data-ttu-id="8cb6c-123">Nazwa usługi migracji danych.</span><span class="sxs-lookup"><span data-stu-id="8cb6c-123">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="8cb6c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cb6c-124">-PassThru</span></span>
<span data-ttu-id="8cb6c-125">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="8cb6c-125">Returns an true/false.</span></span>
<span data-ttu-id="8cb6c-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8cb6c-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8cb6c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cb6c-127">-ResourceGroupName</span></span>
<span data-ttu-id="8cb6c-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8cb6c-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="8cb6c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cb6c-129">-ResourceId</span></span>
<span data-ttu-id="8cb6c-130">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="8cb6c-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="8cb6c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cb6c-131">-WhatIf</span></span>
<span data-ttu-id="8cb6c-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cb6c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cb6c-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8cb6c-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="8cb6c-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8cb6c-134">INPUTS</span></span>

### <span data-ttu-id="8cb6c-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8cb6c-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="8cb6c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8cb6c-136">System.String</span></span>


## <span data-ttu-id="8cb6c-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8cb6c-137">OUTPUTS</span></span>

### <span data-ttu-id="8cb6c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8cb6c-138">System.Boolean</span></span>


## <span data-ttu-id="8cb6c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8cb6c-139">NOTES</span></span>

## <span data-ttu-id="8cb6c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8cb6c-140">RELATED LINKS</span></span>


