---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: ac17206073ff9992c8569da884d1d53c385bccbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705978"
---
# <span data-ttu-id="52789-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="52789-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="52789-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52789-102">SYNOPSIS</span></span>
<span data-ttu-id="52789-103">Usuwa zestaw danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="52789-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="52789-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52789-104">SYNTAX</span></span>

### <span data-ttu-id="52789-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="52789-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52789-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="52789-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52789-107">Opis</span><span class="sxs-lookup"><span data-stu-id="52789-107">DESCRIPTION</span></span>
<span data-ttu-id="52789-108">Polecenie cmdlet **Remove-AzDataFactoryDataset** umożliwia usunięcie zestawu danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="52789-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="52789-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52789-109">EXAMPLES</span></span>

### <span data-ttu-id="52789-110">Przykład 1: usuwanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="52789-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="52789-111">To polecenie usuwa zestaw danych o nazwie DAWikiAggregatedData z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="52789-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="52789-112">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="52789-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="52789-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52789-113">PARAMETERS</span></span>

### <span data-ttu-id="52789-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="52789-114">-DataFactory</span></span>
<span data-ttu-id="52789-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="52789-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="52789-116">To polecenie cmdlet umożliwia usunięcie zestawu danych z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="52789-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52789-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="52789-117">-DataFactoryName</span></span>
<span data-ttu-id="52789-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="52789-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="52789-119">To polecenie cmdlet umożliwia usunięcie zestawu danych z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="52789-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="52789-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52789-120">-DefaultProfile</span></span>
<span data-ttu-id="52789-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="52789-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52789-122">-Force</span><span class="sxs-lookup"><span data-stu-id="52789-122">-Force</span></span>
<span data-ttu-id="52789-123">Wskazuje, że to polecenie cmdlet usunie zestaw danych bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="52789-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="52789-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="52789-124">-Name</span></span>
<span data-ttu-id="52789-125">Określa nazwę zestawu danych, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="52789-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52789-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52789-126">-ResourceGroupName</span></span>
<span data-ttu-id="52789-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="52789-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="52789-128">To polecenie cmdlet umożliwia usunięcie zestawu danych z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="52789-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="52789-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52789-129">-Confirm</span></span>
<span data-ttu-id="52789-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52789-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52789-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52789-131">-WhatIf</span></span>
<span data-ttu-id="52789-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52789-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52789-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="52789-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52789-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52789-134">CommonParameters</span></span>
<span data-ttu-id="52789-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52789-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52789-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52789-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52789-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52789-137">INPUTS</span></span>

### <span data-ttu-id="52789-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="52789-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="52789-139">System. String</span><span class="sxs-lookup"><span data-stu-id="52789-139">System.String</span></span>

## <span data-ttu-id="52789-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52789-140">OUTPUTS</span></span>

### <span data-ttu-id="52789-141">System. void</span><span class="sxs-lookup"><span data-stu-id="52789-141">System.Void</span></span>

## <span data-ttu-id="52789-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52789-142">NOTES</span></span>
* <span data-ttu-id="52789-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="52789-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="52789-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52789-144">RELATED LINKS</span></span>

[<span data-ttu-id="52789-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="52789-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="52789-146">Nowe — AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="52789-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


