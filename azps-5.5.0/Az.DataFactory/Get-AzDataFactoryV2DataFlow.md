---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 7bd25d444a4277e2aa423026be551fab1c5f360e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415159"
---
# <span data-ttu-id="81e9b-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="81e9b-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="81e9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="81e9b-103">Pobiera informacje o przepływach danych w układzie Data Factory.</span><span class="sxs-lookup"><span data-stu-id="81e9b-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="81e9b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="81e9b-104">SYNTAX</span></span>

### <span data-ttu-id="81e9b-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="81e9b-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81e9b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="81e9b-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81e9b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="81e9b-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81e9b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="81e9b-108">DESCRIPTION</span></span>
<span data-ttu-id="81e9b-109">Polecenie Get-AzDataFactoryV2DataFlow pobiera informacje o przepływach danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="81e9b-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="81e9b-110">Jeśli określisz nazwę przepływu danych, to polecenie cmdlet pobiera informacje o tym przepływie danych.</span><span class="sxs-lookup"><span data-stu-id="81e9b-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="81e9b-111">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich przepływach danych w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="81e9b-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="81e9b-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="81e9b-112">EXAMPLES</span></span>
### <span data-ttu-id="81e9b-113">Przykład 1. Uzyskiwanie informacji o wszystkich przepływach danych</span><span class="sxs-lookup"><span data-stu-id="81e9b-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="81e9b-114">To polecenie pobiera informacje o wszystkich przepływach danych w fabrycznej układzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="81e9b-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="81e9b-115">Przykład 2. Uzyskiwanie informacji o określonym przepływie danych</span><span class="sxs-lookup"><span data-stu-id="81e9b-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="81e9b-116">To polecenie pobiera informacje o przepływie danych o nazwie Przepływ danych1 w fabrycznej układzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="81e9b-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="81e9b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81e9b-117">PARAMETERS</span></span>

### <span data-ttu-id="81e9b-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="81e9b-118">-DataFactory</span></span>
<span data-ttu-id="81e9b-119">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="81e9b-119">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81e9b-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="81e9b-120">-DataFactoryName</span></span>
<span data-ttu-id="81e9b-121">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="81e9b-121">The data factory name.</span></span>

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

### <span data-ttu-id="81e9b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e9b-122">-DefaultProfile</span></span>
<span data-ttu-id="81e9b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="81e9b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81e9b-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="81e9b-124">-Name</span></span>
<span data-ttu-id="81e9b-125">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="81e9b-125">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DataFlowName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81e9b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81e9b-126">-ResourceGroupName</span></span>
<span data-ttu-id="81e9b-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81e9b-127">The resource group name.</span></span>

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

### <span data-ttu-id="81e9b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81e9b-128">-ResourceId</span></span>
<span data-ttu-id="81e9b-129">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="81e9b-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="81e9b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e9b-130">CommonParameters</span></span>
<span data-ttu-id="81e9b-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81e9b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e9b-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81e9b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e9b-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81e9b-133">INPUTS</span></span>

### <span data-ttu-id="81e9b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="81e9b-134">System.String</span></span>

### <span data-ttu-id="81e9b-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="81e9b-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="81e9b-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81e9b-136">OUTPUTS</span></span>

### <span data-ttu-id="81e9b-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="81e9b-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="81e9b-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="81e9b-138">NOTES</span></span>
<span data-ttu-id="81e9b-139">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="81e9b-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="81e9b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81e9b-140">RELATED LINKS</span></span>


