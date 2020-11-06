---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Stop-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 59ec77f0c6e3a2f9389931e12ecbce155fe970bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543891"
---
# <span data-ttu-id="da26e-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="da26e-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="da26e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da26e-102">SYNOPSIS</span></span>
<span data-ttu-id="da26e-103">Zatrzymuje wystąpienie usługi migracji bazy danych platformy Azure, która jest w stanie uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="da26e-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da26e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da26e-104">SYNTAX</span></span>

### <span data-ttu-id="da26e-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da26e-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da26e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da26e-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da26e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da26e-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da26e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="da26e-108">DESCRIPTION</span></span>
<span data-ttu-id="da26e-109">Polecenie cmdlet Stop-AzureRmDataMigrationService zatrzymuje wystąpienie usługi migracji bazy danych platformy Azure, która jest w stanie uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="da26e-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="da26e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da26e-110">EXAMPLES</span></span>

### <span data-ttu-id="da26e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da26e-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="da26e-112">W powyższym przykładzie zatrzymano wystąpienie usługi migracji bazy danych platformy Azure o nazwie TestService na podstawie nazwy usługi przekazanej jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="da26e-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="da26e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="da26e-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="da26e-114">W powyższym przykładzie zatrzymano wystąpienie usługi migracji bazy danych platformy Azure opartej na obiekcie PSDataMigrationService przekazanym jako parametr wejściowy.</span><span class="sxs-lookup"><span data-stu-id="da26e-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="da26e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da26e-115">PARAMETERS</span></span>

### <span data-ttu-id="da26e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da26e-116">-DefaultProfile</span></span>
<span data-ttu-id="da26e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da26e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da26e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="da26e-118">-InputObject</span></span>
<span data-ttu-id="da26e-119">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="da26e-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="da26e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da26e-120">-Name</span></span>
<span data-ttu-id="da26e-121">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="da26e-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="da26e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da26e-122">-PassThru</span></span>
<span data-ttu-id="da26e-123">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="da26e-123">Returns an true/false.</span></span>
<span data-ttu-id="da26e-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="da26e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="da26e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da26e-125">-ResourceGroupName</span></span>
<span data-ttu-id="da26e-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="da26e-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="da26e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da26e-127">-ResourceId</span></span>
<span data-ttu-id="da26e-128">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="da26e-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="da26e-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da26e-129">-Confirm</span></span>
<span data-ttu-id="da26e-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da26e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da26e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da26e-131">-WhatIf</span></span>
<span data-ttu-id="da26e-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da26e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da26e-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da26e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da26e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da26e-134">CommonParameters</span></span>
<span data-ttu-id="da26e-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da26e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da26e-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da26e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da26e-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da26e-137">INPUTS</span></span>

### <span data-ttu-id="da26e-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="da26e-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="da26e-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="da26e-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="da26e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="da26e-140">System.String</span></span>

## <span data-ttu-id="da26e-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da26e-141">OUTPUTS</span></span>

### <span data-ttu-id="da26e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da26e-142">System.Boolean</span></span>

## <span data-ttu-id="da26e-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da26e-143">NOTES</span></span>

## <span data-ttu-id="da26e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da26e-144">RELATED LINKS</span></span>
