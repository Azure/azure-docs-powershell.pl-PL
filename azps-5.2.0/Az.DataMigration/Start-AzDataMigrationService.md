---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 2b5c24b3745007cb3a2f48432609490bd38a4186
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328977"
---
# <span data-ttu-id="973af-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="973af-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="973af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="973af-102">SYNOPSIS</span></span>
<span data-ttu-id="973af-103">Powoduje uruchomienie wystąpienia usługi migracji bazy danych platformy Azure w stanie zatrzymanym.</span><span class="sxs-lookup"><span data-stu-id="973af-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="973af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="973af-104">SYNTAX</span></span>

### <span data-ttu-id="973af-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="973af-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="973af-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="973af-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="973af-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="973af-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="973af-108">Opis</span><span class="sxs-lookup"><span data-stu-id="973af-108">DESCRIPTION</span></span>
<span data-ttu-id="973af-109">Polecenie cmdlet Start-AzDataMigrationService uruchamia wystąpienie usługi migracji bazy danych platformy Azure w stanie zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="973af-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="973af-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="973af-110">EXAMPLES</span></span>

### <span data-ttu-id="973af-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="973af-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="973af-112">W powyższym przykładzie rozpoczęto wystąpienie usługi migracji bazy danych platformy Azure o nazwie usługa testowa w stanie zatrzymania na podstawie nazwy usługi przekazanej jako dane wejściowe</span><span class="sxs-lookup"><span data-stu-id="973af-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="973af-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="973af-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="973af-114">W powyższym przykładzie rozpoczęto wystąpienie usługi migracji bazy danych platformy Azure na podstawie PSDataMigrationService przekazana jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="973af-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="973af-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="973af-115">PARAMETERS</span></span>

### <span data-ttu-id="973af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="973af-116">-DefaultProfile</span></span>
<span data-ttu-id="973af-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="973af-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="973af-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="973af-118">-InputObject</span></span>
<span data-ttu-id="973af-119">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="973af-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="973af-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="973af-120">-Name</span></span>
<span data-ttu-id="973af-121">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="973af-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="973af-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="973af-122">-PassThru</span></span>
<span data-ttu-id="973af-123">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="973af-123">Returns an true/false.</span></span>
<span data-ttu-id="973af-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="973af-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="973af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="973af-125">-ResourceGroupName</span></span>
<span data-ttu-id="973af-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="973af-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="973af-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="973af-127">-ResourceId</span></span>
<span data-ttu-id="973af-128">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="973af-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="973af-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="973af-129">-Confirm</span></span>
<span data-ttu-id="973af-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="973af-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="973af-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="973af-131">-WhatIf</span></span>
<span data-ttu-id="973af-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="973af-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="973af-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="973af-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="973af-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="973af-134">CommonParameters</span></span>
<span data-ttu-id="973af-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="973af-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="973af-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="973af-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="973af-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="973af-137">INPUTS</span></span>

### <span data-ttu-id="973af-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="973af-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="973af-139">System. String</span><span class="sxs-lookup"><span data-stu-id="973af-139">System.String</span></span>

## <span data-ttu-id="973af-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="973af-140">OUTPUTS</span></span>

### <span data-ttu-id="973af-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="973af-141">System.Boolean</span></span>

## <span data-ttu-id="973af-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="973af-142">NOTES</span></span>

## <span data-ttu-id="973af-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="973af-143">RELATED LINKS</span></span>
