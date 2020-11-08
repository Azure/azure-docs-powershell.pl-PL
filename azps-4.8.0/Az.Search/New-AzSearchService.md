---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222297"
---
# <span data-ttu-id="933d1-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="933d1-101">New-AzSearchService</span></span>

## <span data-ttu-id="933d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="933d1-102">SYNOPSIS</span></span>
<span data-ttu-id="933d1-103">Tworzy usługę Azure Search.</span><span class="sxs-lookup"><span data-stu-id="933d1-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="933d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="933d1-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="933d1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="933d1-105">DESCRIPTION</span></span>
<span data-ttu-id="933d1-106">Polecenie cmdlet **New-AzSearchService** umożliwia utworzenie usługi Azure Search z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="933d1-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="933d1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="933d1-107">EXAMPLES</span></span>

### <span data-ttu-id="933d1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="933d1-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


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

<span data-ttu-id="933d1-109">Polecenie tworzy usługę Azure Search.</span><span class="sxs-lookup"><span data-stu-id="933d1-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="933d1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="933d1-110">PARAMETERS</span></span>

### <span data-ttu-id="933d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933d1-111">-DefaultProfile</span></span>
<span data-ttu-id="933d1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="933d1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="933d1-113">-Mode</span><span class="sxs-lookup"><span data-stu-id="933d1-113">-HostingMode</span></span>
<span data-ttu-id="933d1-114">Tryb hostingu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="933d1-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="933d1-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="933d1-115">-Location</span></span>
<span data-ttu-id="933d1-116">Lokalizacja usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="933d1-116">Search Service location.</span></span>

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

### <span data-ttu-id="933d1-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="933d1-117">-Name</span></span>
<span data-ttu-id="933d1-118">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="933d1-118">Search Service name.</span></span>

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

### <span data-ttu-id="933d1-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="933d1-119">-PartitionCount</span></span>
<span data-ttu-id="933d1-120">Liczba partycji usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="933d1-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="933d1-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="933d1-121">-ReplicaCount</span></span>
<span data-ttu-id="933d1-122">Liczba replik usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="933d1-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="933d1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="933d1-123">-ResourceGroupName</span></span>
<span data-ttu-id="933d1-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="933d1-124">Resource Group name.</span></span>

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

### <span data-ttu-id="933d1-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="933d1-125">-Sku</span></span>
<span data-ttu-id="933d1-126">SKU usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="933d1-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="933d1-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="933d1-127">-Confirm</span></span>
<span data-ttu-id="933d1-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="933d1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="933d1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="933d1-129">-WhatIf</span></span>
<span data-ttu-id="933d1-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="933d1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="933d1-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="933d1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="933d1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933d1-132">CommonParameters</span></span>
<span data-ttu-id="933d1-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="933d1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933d1-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="933d1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933d1-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="933d1-135">INPUTS</span></span>

### <span data-ttu-id="933d1-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="933d1-136">None</span></span>

## <span data-ttu-id="933d1-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="933d1-137">OUTPUTS</span></span>

### <span data-ttu-id="933d1-138">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="933d1-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="933d1-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="933d1-139">NOTES</span></span>

## <span data-ttu-id="933d1-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="933d1-140">RELATED LINKS</span></span>

[<span data-ttu-id="933d1-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="933d1-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="933d1-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="933d1-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="933d1-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="933d1-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)