---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b4af5eae61e47d8617eb270451f406f349162f50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354457"
---
# <span data-ttu-id="1c4b6-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="1c4b6-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="1c4b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c4b6-102">SYNOPSIS</span></span>
<span data-ttu-id="1c4b6-103">Pobiera informacje o przepływach danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="1c4b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c4b6-104">SYNTAX</span></span>

### <span data-ttu-id="1c4b6-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1c4b6-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c4b6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1c4b6-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c4b6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c4b6-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c4b6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1c4b6-108">DESCRIPTION</span></span>
<span data-ttu-id="1c4b6-109">Polecenie cmdlet Get-AzDataFactoryV2DataFlow pobiera informacje o przepływach danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="1c4b6-110">Jeśli określisz nazwę przepływu danych, to polecenie cmdlet będzie pobierać informacje o przepływie danych.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="1c4b6-111">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o przepływach danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="1c4b6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c4b6-112">EXAMPLES</span></span>
### <span data-ttu-id="1c4b6-113">Przykład 1: uzyskiwanie informacji o przepływach danych</span><span class="sxs-lookup"><span data-stu-id="1c4b6-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="1c4b6-114">To polecenie pobiera informacje dotyczące wszystkich przepływów danych w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="1c4b6-115">Przykład 2: uzyskiwanie informacji o określonym przepływie danych</span><span class="sxs-lookup"><span data-stu-id="1c4b6-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="1c4b6-116">To polecenie pobiera informacje o przepływie danych o nazwie dataflow1 w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="1c4b6-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c4b6-117">PARAMETERS</span></span>

### <span data-ttu-id="1c4b6-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1c4b6-118">-DataFactory</span></span>
<span data-ttu-id="1c4b6-119">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-119">The data factory object.</span></span>

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

### <span data-ttu-id="1c4b6-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1c4b6-120">-DataFactoryName</span></span>
<span data-ttu-id="1c4b6-121">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-121">The data factory name.</span></span>

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

### <span data-ttu-id="1c4b6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c4b6-122">-DefaultProfile</span></span>
<span data-ttu-id="1c4b6-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c4b6-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1c4b6-124">-Name</span></span>
<span data-ttu-id="1c4b6-125">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-125">The data flow name.</span></span>

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

### <span data-ttu-id="1c4b6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c4b6-126">-ResourceGroupName</span></span>
<span data-ttu-id="1c4b6-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-127">The resource group name.</span></span>

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

### <span data-ttu-id="1c4b6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c4b6-128">-ResourceId</span></span>
<span data-ttu-id="1c4b6-129">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1c4b6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c4b6-130">CommonParameters</span></span>
<span data-ttu-id="1c4b6-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c4b6-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c4b6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c4b6-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c4b6-133">INPUTS</span></span>

### <span data-ttu-id="1c4b6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1c4b6-134">System.String</span></span>

### <span data-ttu-id="1c4b6-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1c4b6-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1c4b6-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c4b6-136">OUTPUTS</span></span>

### <span data-ttu-id="1c4b6-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="1c4b6-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="1c4b6-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c4b6-138">NOTES</span></span>
<span data-ttu-id="1c4b6-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="1c4b6-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1c4b6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c4b6-140">RELATED LINKS</span></span>

[<span data-ttu-id="1c4b6-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="1c4b6-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="1c4b6-142">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="1c4b6-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)