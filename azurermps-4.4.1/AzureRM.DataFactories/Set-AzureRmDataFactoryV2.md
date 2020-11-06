---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: b5e5d42ba114da87daa3fa3effb15d3ad8bab22c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525518"
---
# <span data-ttu-id="4ce1f-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4ce1f-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="4ce1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ce1f-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce1f-103">Tworzy fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="4ce1f-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ce1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ce1f-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ce1f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ce1f-105">DESCRIPTION</span></span>
<span data-ttu-id="4ce1f-106">Polecenie cmdlet **Set-AzureRmDataFactoryV2** tworzy fabrykę danych z określoną nazwą i lokalizacją grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ce1f-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="4ce1f-107">Wykonuj następujące operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="4ce1f-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="4ce1f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ce1f-108">EXAMPLES</span></span>

### <span data-ttu-id="4ce1f-109">Przykład 1. Tworzenie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="4ce1f-109">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="4ce1f-110">To polecenie tworzy fabrykę danych o nazwie WikiADF w grupie zasobów o nazwie ADF w lokalizacji na zachód.</span><span class="sxs-lookup"><span data-stu-id="4ce1f-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="4ce1f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ce1f-111">PARAMETERS</span></span>

### <span data-ttu-id="4ce1f-112">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ce1f-112">-Confirm</span></span>
<span data-ttu-id="4ce1f-113">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ce1f-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce1f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4ce1f-114">-Force</span></span>
<span data-ttu-id="4ce1f-115">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4ce1f-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4ce1f-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4ce1f-116">-Location</span></span>
<span data-ttu-id="4ce1f-117">Fabryka danych jest tworzona w tym regionie.</span><span class="sxs-lookup"><span data-stu-id="4ce1f-117">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce1f-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ce1f-118">-Name</span></span>
<span data-ttu-id="4ce1f-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="4ce1f-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce1f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce1f-120">-ResourceGroupName</span></span>
<span data-ttu-id="4ce1f-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ce1f-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce1f-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ce1f-122">-Tag</span></span>
<span data-ttu-id="4ce1f-123">Znaczniki fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="4ce1f-123">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce1f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce1f-124">-WhatIf</span></span>
<span data-ttu-id="4ce1f-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ce1f-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4ce1f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce1f-126">-DefaultProfile</span></span>
<span data-ttu-id="4ce1f-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ce1f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ce1f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce1f-128">CommonParameters</span></span>
<span data-ttu-id="4ce1f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ce1f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce1f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce1f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce1f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ce1f-131">INPUTS</span></span>

### <span data-ttu-id="4ce1f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4ce1f-132">System.String</span></span>
<span data-ttu-id="4ce1f-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4ce1f-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4ce1f-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ce1f-134">OUTPUTS</span></span>

### <span data-ttu-id="4ce1f-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4ce1f-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="4ce1f-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ce1f-136">NOTES</span></span>
<span data-ttu-id="4ce1f-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="4ce1f-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4ce1f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ce1f-138">RELATED LINKS</span></span>

[<span data-ttu-id="4ce1f-139">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4ce1f-139">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="4ce1f-140">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4ce1f-140">Remove-AzureRmDataFactoryV2</span></span>]()
