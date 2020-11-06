---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 35810cf1d190f9ee8ada758fbd2e52fe41ca2455
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525189"
---
# <span data-ttu-id="e7ee7-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="e7ee7-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="e7ee7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7ee7-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ee7-103">Usuwa zestaw danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7ee7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7ee7-104">SYNTAX</span></span>

### <span data-ttu-id="e7ee7-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e7ee7-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ee7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e7ee7-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7ee7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e7ee7-107">DESCRIPTION</span></span>
<span data-ttu-id="e7ee7-108">Polecenie cmdlet **Remove-AzureRmDataFactoryDataset** umożliwia usunięcie zestawu danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="e7ee7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7ee7-109">EXAMPLES</span></span>

### <span data-ttu-id="e7ee7-110">Przykład 1: usuwanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="e7ee7-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="e7ee7-111">To polecenie usuwa zestaw danych o nazwie DAWikiAggregatedData z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="e7ee7-112">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="e7ee7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7ee7-113">PARAMETERS</span></span>

### <span data-ttu-id="e7ee7-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e7ee7-114">-DataFactory</span></span>
<span data-ttu-id="e7ee7-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="e7ee7-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e7ee7-116">To polecenie cmdlet umożliwia usunięcie zestawu danych z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ee7-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e7ee7-117">-DataFactoryName</span></span>
<span data-ttu-id="e7ee7-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e7ee7-119">To polecenie cmdlet umożliwia usunięcie zestawu danych z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ee7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ee7-120">-DefaultProfile</span></span>
<span data-ttu-id="e7ee7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e7ee7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7ee7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e7ee7-122">-Force</span></span>
<span data-ttu-id="e7ee7-123">Wskazuje, że to polecenie cmdlet usunie zestaw danych bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e7ee7-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7ee7-124">-Name</span></span>
<span data-ttu-id="e7ee7-125">Określa nazwę zestawu danych, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ee7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7ee7-126">-ResourceGroupName</span></span>
<span data-ttu-id="e7ee7-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e7ee7-128">To polecenie cmdlet umożliwia usunięcie zestawu danych z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ee7-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7ee7-129">-Confirm</span></span>
<span data-ttu-id="e7ee7-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ee7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7ee7-131">-WhatIf</span></span>
<span data-ttu-id="e7ee7-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7ee7-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ee7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ee7-134">CommonParameters</span></span>
<span data-ttu-id="e7ee7-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ee7-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7ee7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ee7-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7ee7-137">INPUTS</span></span>

### <span data-ttu-id="e7ee7-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e7ee7-138">None</span></span>
<span data-ttu-id="e7ee7-139">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e7ee7-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e7ee7-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7ee7-140">OUTPUTS</span></span>

### <span data-ttu-id="e7ee7-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7ee7-141">System.Boolean</span></span>

## <span data-ttu-id="e7ee7-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7ee7-142">NOTES</span></span>
* <span data-ttu-id="e7ee7-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="e7ee7-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e7ee7-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7ee7-144">RELATED LINKS</span></span>

[<span data-ttu-id="e7ee7-145">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="e7ee7-145">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="e7ee7-146">Nowe — AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="e7ee7-146">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)


