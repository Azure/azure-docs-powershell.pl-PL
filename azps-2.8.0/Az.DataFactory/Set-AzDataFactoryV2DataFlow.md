---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 7938a4b9b96cbbd61d0bb484ddc3129dfd23f215
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411521"
---
# <span data-ttu-id="e4c45-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="e4c45-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="e4c45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4c45-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c45-103">Tworzy przepływ danych w układzie Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e4c45-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="e4c45-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e4c45-104">SYNTAX</span></span>

### <span data-ttu-id="e4c45-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="e4c45-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4c45-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e4c45-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4c45-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e4c45-107">DESCRIPTION</span></span>
<span data-ttu-id="e4c45-108">Polecenie Set-AzDataFactoryV2DataFlow cmdlet tworzy przepływ danych lub aktualizuje istniejący przepływ danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e4c45-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="e4c45-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e4c45-109">EXAMPLES</span></span>

### <span data-ttu-id="e4c45-110">Przykład 1. Tworzenie przepływu danych</span><span class="sxs-lookup"><span data-stu-id="e4c45-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="e4c45-111">To polecenie tworzy przepływ danych o nazwie Naddemo1 w fabrycznej układzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e4c45-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="e4c45-112">To polecenie bazuje na przepływie danych na podstawie informacji TaxiDemo1.jspliku.</span><span class="sxs-lookup"><span data-stu-id="e4c45-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="e4c45-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4c45-113">PARAMETERS</span></span>

### <span data-ttu-id="e4c45-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e4c45-114">-DataFactoryName</span></span>
<span data-ttu-id="e4c45-115">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="e4c45-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4c45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c45-116">-DefaultProfile</span></span>
<span data-ttu-id="e4c45-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4c45-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4c45-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e4c45-118">-DefinitionFile</span></span>
<span data-ttu-id="e4c45-119">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="e4c45-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4c45-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e4c45-120">-Force</span></span>
<span data-ttu-id="e4c45-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e4c45-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e4c45-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e4c45-122">-Name</span></span>
<span data-ttu-id="e4c45-123">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="e4c45-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4c45-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c45-124">-ResourceGroupName</span></span>
<span data-ttu-id="e4c45-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4c45-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4c45-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4c45-126">-ResourceId</span></span>
<span data-ttu-id="e4c45-127">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="e4c45-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4c45-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4c45-128">-Confirm</span></span>
<span data-ttu-id="e4c45-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e4c45-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4c45-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4c45-130">-WhatIf</span></span>
<span data-ttu-id="e4c45-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4c45-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4c45-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e4c45-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4c45-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c45-133">CommonParameters</span></span>
<span data-ttu-id="e4c45-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4c45-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c45-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4c45-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c45-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4c45-136">INPUTS</span></span>

### <span data-ttu-id="e4c45-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e4c45-137">System.String</span></span>

## <span data-ttu-id="e4c45-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e4c45-138">OUTPUTS</span></span>

### <span data-ttu-id="e4c45-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="e4c45-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="e4c45-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e4c45-140">NOTES</span></span>
<span data-ttu-id="e4c45-141">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="e4c45-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e4c45-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4c45-142">RELATED LINKS</span></span>


