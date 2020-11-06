---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: f0fcfd8a99bd28f01077257e48c0dc9662973751
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525157"
---
# <span data-ttu-id="0182b-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0182b-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="0182b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0182b-102">SYNOPSIS</span></span>
<span data-ttu-id="0182b-103">Tworzy fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="0182b-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0182b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0182b-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0182b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0182b-105">DESCRIPTION</span></span>
<span data-ttu-id="0182b-106">Polecenie cmdlet **Set-AzureRmDataFactoryV2** tworzy fabrykę danych z określoną nazwą i lokalizacją grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0182b-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="0182b-107">Wykonuj następujące operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="0182b-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="0182b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0182b-108">EXAMPLES</span></span>

### <span data-ttu-id="0182b-109">Przykład 1. Tworzenie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="0182b-109">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="0182b-110">To polecenie tworzy fabrykę danych o nazwie WikiADF w grupie zasobów o nazwie ADF w lokalizacji na zachód.</span><span class="sxs-lookup"><span data-stu-id="0182b-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="0182b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0182b-111">PARAMETERS</span></span>

### <span data-ttu-id="0182b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0182b-112">-DefaultProfile</span></span>
<span data-ttu-id="0182b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0182b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0182b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="0182b-114">-Force</span></span>
<span data-ttu-id="0182b-115">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0182b-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0182b-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0182b-116">-Location</span></span>
<span data-ttu-id="0182b-117">Fabryka danych jest tworzona w tym regionie.</span><span class="sxs-lookup"><span data-stu-id="0182b-117">The data factory is created in this region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0182b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0182b-118">-Name</span></span>
<span data-ttu-id="0182b-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0182b-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0182b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0182b-120">-ResourceGroupName</span></span>
<span data-ttu-id="0182b-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0182b-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0182b-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="0182b-122">-Tag</span></span>
<span data-ttu-id="0182b-123">Znaczniki fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0182b-123">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0182b-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0182b-124">-Confirm</span></span>
<span data-ttu-id="0182b-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0182b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0182b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0182b-126">-WhatIf</span></span>
<span data-ttu-id="0182b-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0182b-127">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0182b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0182b-128">CommonParameters</span></span>
<span data-ttu-id="0182b-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0182b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0182b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0182b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0182b-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0182b-131">INPUTS</span></span>

### <span data-ttu-id="0182b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0182b-132">System.String</span></span>
<span data-ttu-id="0182b-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0182b-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0182b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0182b-134">OUTPUTS</span></span>

### <span data-ttu-id="0182b-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0182b-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0182b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0182b-136">NOTES</span></span>
<span data-ttu-id="0182b-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="0182b-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0182b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0182b-138">RELATED LINKS</span></span>

[<span data-ttu-id="0182b-139">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0182b-139">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="0182b-140">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0182b-140">Remove-AzureRmDataFactoryV2</span></span>]()
