---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: c50023cefbae9a9ba341eba22f40a421c37d12c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545415"
---
# <span data-ttu-id="d8197-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d8197-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="d8197-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8197-102">SYNOPSIS</span></span>
<span data-ttu-id="d8197-103">Tworzy fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="d8197-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8197-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8197-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8197-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8197-105">DESCRIPTION</span></span>
<span data-ttu-id="d8197-106">Polecenie cmdlet **Set-AzureRmDataFactoryV2** tworzy fabrykę danych z określoną nazwą i lokalizacją grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8197-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="d8197-107">Wykonuj następujące operacje w następującej kolejności:--Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d8197-107">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="d8197-108">--Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="d8197-108">-- Create linked services.</span></span>
<span data-ttu-id="d8197-109">--Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="d8197-109">-- Create datasets.</span></span>
<span data-ttu-id="d8197-110">— Utwórz rurociąg.</span><span class="sxs-lookup"><span data-stu-id="d8197-110">-- Create a pipeline.</span></span>

## <span data-ttu-id="d8197-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8197-111">EXAMPLES</span></span>

### <span data-ttu-id="d8197-112">Przykład 1. Tworzenie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="d8197-112">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="d8197-113">To polecenie tworzy fabrykę danych o nazwie WikiADF w grupie zasobów o nazwie ADF w lokalizacji na zachód.</span><span class="sxs-lookup"><span data-stu-id="d8197-113">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="d8197-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8197-114">PARAMETERS</span></span>

### <span data-ttu-id="d8197-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8197-115">-DefaultProfile</span></span>
<span data-ttu-id="d8197-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8197-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8197-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d8197-117">-Force</span></span>
<span data-ttu-id="d8197-118">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d8197-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d8197-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d8197-119">-Location</span></span>
<span data-ttu-id="d8197-120">Fabryka danych jest tworzona w tym regionie.</span><span class="sxs-lookup"><span data-stu-id="d8197-120">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="d8197-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d8197-121">-Name</span></span>
<span data-ttu-id="d8197-122">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d8197-122">The data factory name.</span></span>

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

### <span data-ttu-id="d8197-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8197-123">-ResourceGroupName</span></span>
<span data-ttu-id="d8197-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8197-124">The resource group name.</span></span>

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

### <span data-ttu-id="d8197-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="d8197-125">-Tag</span></span>
<span data-ttu-id="d8197-126">Znaczniki fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d8197-126">The tags of the data factory.</span></span>

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

### <span data-ttu-id="d8197-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8197-127">-Confirm</span></span>
<span data-ttu-id="d8197-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8197-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8197-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8197-129">-WhatIf</span></span>
<span data-ttu-id="d8197-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8197-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d8197-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8197-131">CommonParameters</span></span>
<span data-ttu-id="d8197-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8197-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8197-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8197-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8197-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8197-134">INPUTS</span></span>

### <span data-ttu-id="d8197-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d8197-135">System.String</span></span>

### <span data-ttu-id="d8197-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d8197-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d8197-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8197-137">OUTPUTS</span></span>

### <span data-ttu-id="d8197-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d8197-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d8197-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8197-139">NOTES</span></span>
<span data-ttu-id="d8197-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="d8197-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d8197-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8197-141">RELATED LINKS</span></span>

[<span data-ttu-id="d8197-142">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d8197-142">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="d8197-143">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d8197-143">Remove-AzureRmDataFactoryV2</span></span>]()
