---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 42d9de3f23f1aca904aa0f42722217d0b9bf8a3a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501549"
---
# <span data-ttu-id="861bb-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="861bb-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="861bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="861bb-102">SYNOPSIS</span></span>
<span data-ttu-id="861bb-103">Umożliwia utworzenie przepływu danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="861bb-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="861bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="861bb-104">SYNTAX</span></span>

### <span data-ttu-id="861bb-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="861bb-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="861bb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="861bb-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="861bb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="861bb-107">DESCRIPTION</span></span>
<span data-ttu-id="861bb-108">Polecenie cmdlet Set-AzDataFactoryV2DataFlow powoduje utworzenie przepływu danych lub zaktualizowanie istniejącego przepływu danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="861bb-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="861bb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="861bb-109">EXAMPLES</span></span>

### <span data-ttu-id="861bb-110">Przykład 1. Tworzenie przepływu danych</span><span class="sxs-lookup"><span data-stu-id="861bb-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="861bb-111">To polecenie tworzy przepływ danych o nazwie TaxiDemo1 w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="861bb-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="861bb-112">Polecenie opiera się na przeniesieniu przepływu danych na informacjach w TaxiDemo1.jspliku.</span><span class="sxs-lookup"><span data-stu-id="861bb-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="861bb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="861bb-113">PARAMETERS</span></span>

### <span data-ttu-id="861bb-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="861bb-114">-DataFactoryName</span></span>
<span data-ttu-id="861bb-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="861bb-115">The data factory name.</span></span>

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

### <span data-ttu-id="861bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="861bb-116">-DefaultProfile</span></span>
<span data-ttu-id="861bb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="861bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="861bb-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="861bb-118">-DefinitionFile</span></span>
<span data-ttu-id="861bb-119">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="861bb-119">The JSON file path.</span></span>

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

### <span data-ttu-id="861bb-120">-Force</span><span class="sxs-lookup"><span data-stu-id="861bb-120">-Force</span></span>
<span data-ttu-id="861bb-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="861bb-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="861bb-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="861bb-122">-Name</span></span>
<span data-ttu-id="861bb-123">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="861bb-123">The data flow name.</span></span>

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

### <span data-ttu-id="861bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="861bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="861bb-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="861bb-125">The resource group name.</span></span>

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

### <span data-ttu-id="861bb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="861bb-126">-ResourceId</span></span>
<span data-ttu-id="861bb-127">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="861bb-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="861bb-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="861bb-128">-Confirm</span></span>
<span data-ttu-id="861bb-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="861bb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="861bb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="861bb-130">-WhatIf</span></span>
<span data-ttu-id="861bb-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="861bb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="861bb-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="861bb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="861bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="861bb-133">CommonParameters</span></span>
<span data-ttu-id="861bb-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="861bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="861bb-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="861bb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="861bb-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="861bb-136">INPUTS</span></span>

### <span data-ttu-id="861bb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="861bb-137">System.String</span></span>

## <span data-ttu-id="861bb-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="861bb-138">OUTPUTS</span></span>

### <span data-ttu-id="861bb-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="861bb-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="861bb-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="861bb-140">NOTES</span></span>
<span data-ttu-id="861bb-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="861bb-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="861bb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="861bb-142">RELATED LINKS</span></span>

[<span data-ttu-id="861bb-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="861bb-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="861bb-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="861bb-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
