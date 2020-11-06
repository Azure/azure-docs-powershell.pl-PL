---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchService.md
ms.openlocfilehash: 934ba85d438178ee636d5042f1fa145e63d60291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543464"
---
# <span data-ttu-id="58156-101">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="58156-101">New-AzureRmSearchService</span></span>

## <span data-ttu-id="58156-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58156-102">SYNOPSIS</span></span>
<span data-ttu-id="58156-103">Tworzy usługę Azure Search.</span><span class="sxs-lookup"><span data-stu-id="58156-103">Creates an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58156-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58156-104">SYNTAX</span></span>

```
New-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58156-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58156-105">DESCRIPTION</span></span>
<span data-ttu-id="58156-106">Polecenie cmdlet **New-AzureRmSearchService** umożliwia utworzenie usługi Azure Search z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="58156-106">The **New-AzureRmSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="58156-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58156-107">EXAMPLES</span></span>

### <span data-ttu-id="58156-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58156-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="58156-109">Polecenie tworzy usługę Azure Search.</span><span class="sxs-lookup"><span data-stu-id="58156-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="58156-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58156-110">PARAMETERS</span></span>

### <span data-ttu-id="58156-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58156-111">-DefaultProfile</span></span>
<span data-ttu-id="58156-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58156-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58156-113">-Mode</span><span class="sxs-lookup"><span data-stu-id="58156-113">-HostingMode</span></span>
<span data-ttu-id="58156-114">Tryb hostingu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="58156-114">Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58156-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="58156-115">-Location</span></span>
<span data-ttu-id="58156-116">Lokalizacja usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="58156-116">Search Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58156-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="58156-117">-Name</span></span>
<span data-ttu-id="58156-118">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="58156-118">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58156-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="58156-119">-PartitionCount</span></span>
<span data-ttu-id="58156-120">Liczba partycji usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="58156-120">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58156-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="58156-121">-ReplicaCount</span></span>
<span data-ttu-id="58156-122">Liczba replik usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="58156-122">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58156-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58156-123">-ResourceGroupName</span></span>
<span data-ttu-id="58156-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="58156-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58156-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="58156-125">-Sku</span></span>
<span data-ttu-id="58156-126">SKU usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="58156-126">Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58156-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58156-127">-Confirm</span></span>
<span data-ttu-id="58156-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58156-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58156-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58156-129">-WhatIf</span></span>
<span data-ttu-id="58156-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58156-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58156-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58156-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58156-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58156-132">CommonParameters</span></span>
<span data-ttu-id="58156-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58156-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58156-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58156-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58156-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58156-135">INPUTS</span></span>

### <span data-ttu-id="58156-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="58156-136">None</span></span>

## <span data-ttu-id="58156-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58156-137">OUTPUTS</span></span>

### <span data-ttu-id="58156-138">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="58156-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="58156-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58156-139">NOTES</span></span>

## <span data-ttu-id="58156-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58156-140">RELATED LINKS</span></span>

[<span data-ttu-id="58156-141">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="58156-141">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="58156-142">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="58156-142">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="58156-143">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="58156-143">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
