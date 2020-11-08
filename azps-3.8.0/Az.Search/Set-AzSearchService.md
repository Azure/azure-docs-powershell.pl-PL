---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: e4329c0d3ad4499af1174458ea3e0449672774a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052449"
---
# <span data-ttu-id="a4866-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="a4866-101">Set-AzSearchService</span></span>

## <span data-ttu-id="a4866-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4866-102">SYNOPSIS</span></span>
<span data-ttu-id="a4866-103">Aktualizowanie usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="a4866-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="a4866-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4866-104">SYNTAX</span></span>

### <span data-ttu-id="a4866-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a4866-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4866-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4866-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4866-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4866-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4866-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a4866-108">DESCRIPTION</span></span>
<span data-ttu-id="a4866-109">Polecenie cmdlet **Set-AzSearchService** modyfikuje usługę Azure Search.</span><span class="sxs-lookup"><span data-stu-id="a4866-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="a4866-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4866-110">EXAMPLES</span></span>

### <span data-ttu-id="a4866-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4866-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


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

<span data-ttu-id="a4866-112">Przykładowa zmiana liczby partycji i liczby replik usługi wyszukiwania w usłudze Azure to 2.</span><span class="sxs-lookup"><span data-stu-id="a4866-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="a4866-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4866-113">PARAMETERS</span></span>

### <span data-ttu-id="a4866-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4866-114">-DefaultProfile</span></span>
<span data-ttu-id="a4866-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4866-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4866-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a4866-116">-InputObject</span></span>
<span data-ttu-id="a4866-117">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a4866-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="a4866-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4866-118">-Name</span></span>
<span data-ttu-id="a4866-119">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a4866-119">Search Service name.</span></span>

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

### <span data-ttu-id="a4866-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="a4866-120">-PartitionCount</span></span>
<span data-ttu-id="a4866-121">Liczba partycji usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a4866-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="a4866-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="a4866-122">-ReplicaCount</span></span>
<span data-ttu-id="a4866-123">Liczba replik usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a4866-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="a4866-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4866-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4866-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4866-125">Resource Group name.</span></span>

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

### <span data-ttu-id="a4866-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4866-126">-ResourceId</span></span>
<span data-ttu-id="a4866-127">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a4866-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="a4866-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4866-128">-Confirm</span></span>
<span data-ttu-id="a4866-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4866-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4866-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4866-130">-WhatIf</span></span>
<span data-ttu-id="a4866-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4866-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4866-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4866-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4866-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4866-133">CommonParameters</span></span>
<span data-ttu-id="a4866-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4866-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4866-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4866-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4866-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4866-136">INPUTS</span></span>

### <span data-ttu-id="a4866-137">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a4866-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="a4866-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a4866-138">System.String</span></span>

## <span data-ttu-id="a4866-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4866-139">OUTPUTS</span></span>

### <span data-ttu-id="a4866-140">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a4866-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="a4866-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4866-141">NOTES</span></span>

## <span data-ttu-id="a4866-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4866-142">RELATED LINKS</span></span>

[<span data-ttu-id="a4866-143">Nowe — AzSearchService</span><span class="sxs-lookup"><span data-stu-id="a4866-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="a4866-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="a4866-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="a4866-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="a4866-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)