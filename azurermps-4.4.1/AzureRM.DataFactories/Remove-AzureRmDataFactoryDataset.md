---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 85e9e96db366adcb30494ac22e7d1b73bbff9f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527670"
---
# <span data-ttu-id="65eaf-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="65eaf-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="65eaf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="65eaf-103">Usuwa zestaw danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="65eaf-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65eaf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65eaf-104">SYNTAX</span></span>

### <span data-ttu-id="65eaf-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="65eaf-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65eaf-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="65eaf-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65eaf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="65eaf-107">DESCRIPTION</span></span>
<span data-ttu-id="65eaf-108">Polecenie cmdlet **Remove-AzureRmDataFactoryDataset** umożliwia usunięcie zestawu danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="65eaf-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="65eaf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65eaf-109">EXAMPLES</span></span>

### <span data-ttu-id="65eaf-110">Przykład 1: usuwanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="65eaf-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="65eaf-111">To polecenie usuwa zestaw danych o nazwie DAWikiAggregatedData z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="65eaf-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="65eaf-112">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="65eaf-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="65eaf-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65eaf-113">PARAMETERS</span></span>

### <span data-ttu-id="65eaf-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="65eaf-114">-DataFactory</span></span>
<span data-ttu-id="65eaf-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="65eaf-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="65eaf-116">To polecenie cmdlet umożliwia usunięcie zestawu danych z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="65eaf-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="65eaf-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="65eaf-117">-DataFactoryName</span></span>
<span data-ttu-id="65eaf-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="65eaf-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="65eaf-119">To polecenie cmdlet umożliwia usunięcie zestawu danych z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="65eaf-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="65eaf-120">-Force</span><span class="sxs-lookup"><span data-stu-id="65eaf-120">-Force</span></span>
<span data-ttu-id="65eaf-121">Wskazuje, że to polecenie cmdlet usunie zestaw danych bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="65eaf-121">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="65eaf-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65eaf-122">-Name</span></span>
<span data-ttu-id="65eaf-123">Określa nazwę zestawu danych, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="65eaf-123">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="65eaf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65eaf-124">-ResourceGroupName</span></span>
<span data-ttu-id="65eaf-125">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="65eaf-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="65eaf-126">To polecenie cmdlet umożliwia usunięcie zestawu danych z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="65eaf-126">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="65eaf-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65eaf-127">-Confirm</span></span>
<span data-ttu-id="65eaf-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65eaf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65eaf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65eaf-129">-WhatIf</span></span>
<span data-ttu-id="65eaf-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65eaf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65eaf-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65eaf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65eaf-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65eaf-132">-DefaultProfile</span></span>
<span data-ttu-id="65eaf-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65eaf-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65eaf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65eaf-134">CommonParameters</span></span>
<span data-ttu-id="65eaf-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65eaf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65eaf-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65eaf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65eaf-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65eaf-137">INPUTS</span></span>

## <span data-ttu-id="65eaf-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65eaf-138">OUTPUTS</span></span>

### <span data-ttu-id="65eaf-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65eaf-139">System.Boolean</span></span>

## <span data-ttu-id="65eaf-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65eaf-140">NOTES</span></span>
* <span data-ttu-id="65eaf-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="65eaf-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="65eaf-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65eaf-142">RELATED LINKS</span></span>

[<span data-ttu-id="65eaf-143">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="65eaf-143">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="65eaf-144">Nowe — AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="65eaf-144">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)


