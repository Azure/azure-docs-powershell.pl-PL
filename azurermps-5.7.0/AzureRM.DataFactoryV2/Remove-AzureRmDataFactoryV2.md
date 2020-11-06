---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: 330bcf3622faa515a58ea8f1e087d1383b9f154a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525182"
---
# <span data-ttu-id="4275f-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4275f-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="4275f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4275f-102">SYNOPSIS</span></span>
<span data-ttu-id="4275f-103">Usuwa fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="4275f-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4275f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4275f-104">SYNTAX</span></span>

### <span data-ttu-id="4275f-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4275f-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4275f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4275f-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4275f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4275f-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4275f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4275f-108">DESCRIPTION</span></span>
<span data-ttu-id="4275f-109">Polecenie cmdlet Remove-AzureRmDataFactoryV2 powoduje usunięcie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="4275f-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="4275f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4275f-110">EXAMPLES</span></span>

### <span data-ttu-id="4275f-111">Przykład 1: usuwanie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="4275f-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="4275f-112">To polecenie usuwa fabrykę danych o nazwie WikiADF z grupy zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="4275f-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="4275f-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="4275f-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="4275f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4275f-114">PARAMETERS</span></span>

### <span data-ttu-id="4275f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4275f-115">-DefaultProfile</span></span>
<span data-ttu-id="4275f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4275f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4275f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4275f-117">-Force</span></span>
<span data-ttu-id="4275f-118">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4275f-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4275f-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4275f-119">-InputObject</span></span>
<span data-ttu-id="4275f-120">Określa obiekt DataFactory, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="4275f-120">Specifies the DataFactory object to remove.</span></span>

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

### <span data-ttu-id="4275f-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4275f-121">-Name</span></span>
<span data-ttu-id="4275f-122">Określa nazwę fabryki danych, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="4275f-122">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="4275f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4275f-123">-ResourceGroupName</span></span>
<span data-ttu-id="4275f-124">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4275f-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4275f-125">To polecenie cmdlet umożliwia usunięcie fabryki danych z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="4275f-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4275f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4275f-126">-ResourceId</span></span>
<span data-ttu-id="4275f-127">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4275f-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4275f-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4275f-128">-Confirm</span></span>
<span data-ttu-id="4275f-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4275f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4275f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4275f-130">-WhatIf</span></span>
<span data-ttu-id="4275f-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4275f-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4275f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4275f-132">CommonParameters</span></span>
<span data-ttu-id="4275f-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4275f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4275f-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4275f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4275f-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4275f-135">INPUTS</span></span>

### <span data-ttu-id="4275f-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4275f-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="4275f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4275f-137">System.String</span></span>

## <span data-ttu-id="4275f-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4275f-138">OUTPUTS</span></span>

### <span data-ttu-id="4275f-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="4275f-139">System.Object</span></span>

## <span data-ttu-id="4275f-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4275f-140">NOTES</span></span>
<span data-ttu-id="4275f-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="4275f-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4275f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4275f-142">RELATED LINKS</span></span>

[<span data-ttu-id="4275f-143">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4275f-143">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="4275f-144">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4275f-144">Set-AzureRmDataFactoryV2</span></span>]()
