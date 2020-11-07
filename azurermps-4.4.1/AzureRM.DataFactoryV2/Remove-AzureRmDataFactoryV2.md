---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 73cc7df9dcb32dac592df56f16ad819219e06b7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718540"
---
# <span data-ttu-id="13d18-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="13d18-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="13d18-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13d18-102">SYNOPSIS</span></span>
<span data-ttu-id="13d18-103">Usuwa fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="13d18-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13d18-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13d18-104">SYNTAX</span></span>

### <span data-ttu-id="13d18-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="13d18-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="13d18-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="13d18-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="13d18-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13d18-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="13d18-108">Opis</span><span class="sxs-lookup"><span data-stu-id="13d18-108">DESCRIPTION</span></span>
<span data-ttu-id="13d18-109">Polecenie cmdlet Remove-AzureRmDataFactoryV2 powoduje usunięcie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="13d18-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="13d18-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13d18-110">EXAMPLES</span></span>

### <span data-ttu-id="13d18-111">Przykład 1: usuwanie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="13d18-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="13d18-112">To polecenie usuwa fabrykę danych o nazwie WikiADF z grupy zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="13d18-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="13d18-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="13d18-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="13d18-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13d18-114">PARAMETERS</span></span>

### <span data-ttu-id="13d18-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13d18-115">-Confirm</span></span>
<span data-ttu-id="13d18-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13d18-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d18-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="13d18-117">-InputObject</span></span>
<span data-ttu-id="13d18-118">Określa obiekt DataFactory, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="13d18-118">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13d18-119">-Force</span><span class="sxs-lookup"><span data-stu-id="13d18-119">-Force</span></span>
<span data-ttu-id="13d18-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="13d18-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="13d18-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13d18-121">-Name</span></span>
<span data-ttu-id="13d18-122">Określa nazwę fabryki danych, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="13d18-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d18-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13d18-123">-ResourceGroupName</span></span>
<span data-ttu-id="13d18-124">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="13d18-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="13d18-125">To polecenie cmdlet umożliwia usunięcie fabryki danych z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="13d18-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d18-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13d18-126">-ResourceId</span></span>
<span data-ttu-id="13d18-127">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="13d18-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13d18-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13d18-128">-WhatIf</span></span>
<span data-ttu-id="13d18-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13d18-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="13d18-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13d18-130">INPUTS</span></span>

### <span data-ttu-id="13d18-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="13d18-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="13d18-132">System. String</span><span class="sxs-lookup"><span data-stu-id="13d18-132">System.String</span></span>


## <span data-ttu-id="13d18-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13d18-133">OUTPUTS</span></span>

### <span data-ttu-id="13d18-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="13d18-134">System.Object</span></span>

## <span data-ttu-id="13d18-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13d18-135">NOTES</span></span>
<span data-ttu-id="13d18-136">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="13d18-136">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="13d18-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13d18-137">RELATED LINKS</span></span>
[<span data-ttu-id="13d18-138">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="13d18-138">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="13d18-139">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="13d18-139">Set-AzureRmDataFactoryV2</span></span>]()
