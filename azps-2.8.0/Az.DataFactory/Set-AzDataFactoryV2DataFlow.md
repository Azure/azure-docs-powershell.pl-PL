---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: a563d6b0e72c60632d99df2668552b649ffb1662
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705936"
---
# <span data-ttu-id="8007b-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="8007b-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="8007b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8007b-102">SYNOPSIS</span></span>
<span data-ttu-id="8007b-103">Umożliwia utworzenie przepływu danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="8007b-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="8007b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8007b-104">SYNTAX</span></span>

### <span data-ttu-id="8007b-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8007b-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8007b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8007b-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8007b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8007b-107">DESCRIPTION</span></span>
<span data-ttu-id="8007b-108">Polecenie cmdlet Set-AzDataFactoryV2DataFlow powoduje utworzenie przepływu danych lub zaktualizowanie istniejącego przepływu danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8007b-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="8007b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8007b-109">EXAMPLES</span></span>

### <span data-ttu-id="8007b-110">Przykład 1. Tworzenie przepływu danych</span><span class="sxs-lookup"><span data-stu-id="8007b-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="8007b-111">To polecenie tworzy przepływ danych o nazwie TaxiDemo1 w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8007b-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="8007b-112">Polecenie opiera się na przeniesieniu przepływu danych na informacjach w TaxiDemo1.jspliku.</span><span class="sxs-lookup"><span data-stu-id="8007b-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="8007b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8007b-113">PARAMETERS</span></span>

### <span data-ttu-id="8007b-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8007b-114">-DataFactoryName</span></span>
<span data-ttu-id="8007b-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="8007b-115">The data factory name.</span></span>

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

### <span data-ttu-id="8007b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8007b-116">-DefaultProfile</span></span>
<span data-ttu-id="8007b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8007b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8007b-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="8007b-118">-DefinitionFile</span></span>
<span data-ttu-id="8007b-119">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="8007b-119">The JSON file path.</span></span>

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

### <span data-ttu-id="8007b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8007b-120">-Force</span></span>
<span data-ttu-id="8007b-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8007b-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8007b-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8007b-122">-Name</span></span>
<span data-ttu-id="8007b-123">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="8007b-123">The data flow name.</span></span>

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

### <span data-ttu-id="8007b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8007b-124">-ResourceGroupName</span></span>
<span data-ttu-id="8007b-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8007b-125">The resource group name.</span></span>

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

### <span data-ttu-id="8007b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8007b-126">-ResourceId</span></span>
<span data-ttu-id="8007b-127">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8007b-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8007b-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8007b-128">-Confirm</span></span>
<span data-ttu-id="8007b-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8007b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8007b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8007b-130">-WhatIf</span></span>
<span data-ttu-id="8007b-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8007b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8007b-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8007b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8007b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8007b-133">CommonParameters</span></span>
<span data-ttu-id="8007b-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8007b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8007b-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8007b-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8007b-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8007b-136">INPUTS</span></span>

### <span data-ttu-id="8007b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8007b-137">System.String</span></span>

## <span data-ttu-id="8007b-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8007b-138">OUTPUTS</span></span>

### <span data-ttu-id="8007b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="8007b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="8007b-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8007b-140">NOTES</span></span>
<span data-ttu-id="8007b-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="8007b-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8007b-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8007b-142">RELATED LINKS</span></span>

[<span data-ttu-id="8007b-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="8007b-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="8007b-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="8007b-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)