---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/set-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
ms.openlocfilehash: c938dd611d9f6d731c07d5aee76cb390838f4679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543459"
---
# <span data-ttu-id="6c9fc-101">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="6c9fc-101">Set-AzureRmSearchService</span></span>

## <span data-ttu-id="6c9fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c9fc-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9fc-103">Aktualizowanie usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-103">Update an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c9fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c9fc-104">SYNTAX</span></span>

### <span data-ttu-id="6c9fc-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6c9fc-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c9fc-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c9fc-106">InputObjectParameterSet</span></span>
```
Set-AzureRmSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c9fc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c9fc-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c9fc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6c9fc-108">DESCRIPTION</span></span>
<span data-ttu-id="6c9fc-109">Polecenie cmdlet **Set-AzureRmSearchService** modyfikuje usługę Azure Search.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-109">The **Set-AzureRmSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="6c9fc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c9fc-110">EXAMPLES</span></span>

### <span data-ttu-id="6c9fc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c9fc-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="6c9fc-112">Przykładowa zmiana liczby partycji i liczby replik usługi wyszukiwania w usłudze Azure to 2.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="6c9fc-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c9fc-113">PARAMETERS</span></span>

### <span data-ttu-id="6c9fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9fc-114">-DefaultProfile</span></span>
<span data-ttu-id="6c9fc-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c9fc-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6c9fc-116">-InputObject</span></span>
<span data-ttu-id="6c9fc-117">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-117">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9fc-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c9fc-118">-Name</span></span>
<span data-ttu-id="6c9fc-119">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-119">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9fc-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="6c9fc-120">-PartitionCount</span></span>
<span data-ttu-id="6c9fc-121">Liczba partycji usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="6c9fc-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="6c9fc-122">-ReplicaCount</span></span>
<span data-ttu-id="6c9fc-123">Liczba replik usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="6c9fc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c9fc-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c9fc-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9fc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c9fc-126">-ResourceId</span></span>
<span data-ttu-id="6c9fc-127">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-127">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9fc-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c9fc-128">-Confirm</span></span>
<span data-ttu-id="6c9fc-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c9fc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c9fc-130">-WhatIf</span></span>
<span data-ttu-id="6c9fc-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c9fc-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c9fc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9fc-133">CommonParameters</span></span>
<span data-ttu-id="6c9fc-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9fc-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c9fc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9fc-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c9fc-136">INPUTS</span></span>

### <span data-ttu-id="6c9fc-137">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="6c9fc-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="6c9fc-138">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c9fc-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="6c9fc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6c9fc-139">System.String</span></span>

## <span data-ttu-id="6c9fc-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c9fc-140">OUTPUTS</span></span>

### <span data-ttu-id="6c9fc-141">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="6c9fc-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="6c9fc-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c9fc-142">NOTES</span></span>

## <span data-ttu-id="6c9fc-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c9fc-143">RELATED LINKS</span></span>

[<span data-ttu-id="6c9fc-144">Nowe — AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="6c9fc-144">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="6c9fc-145">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="6c9fc-145">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="6c9fc-146">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="6c9fc-146">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
