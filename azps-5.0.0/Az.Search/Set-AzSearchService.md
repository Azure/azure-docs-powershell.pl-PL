---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: e4329c0d3ad4499af1174458ea3e0449672774a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232655"
---
# <span data-ttu-id="0f8f3-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0f8f3-101">Set-AzSearchService</span></span>

## <span data-ttu-id="0f8f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="0f8f3-103">Aktualizowanie usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="0f8f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f8f3-104">SYNTAX</span></span>

### <span data-ttu-id="0f8f3-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0f8f3-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f8f3-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f8f3-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f8f3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f8f3-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f8f3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0f8f3-108">DESCRIPTION</span></span>
<span data-ttu-id="0f8f3-109">Polecenie cmdlet **Set-AzSearchService** modyfikuje usługę Azure Search.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="0f8f3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f8f3-110">EXAMPLES</span></span>

### <span data-ttu-id="0f8f3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0f8f3-111">Example 1</span></span>
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

<span data-ttu-id="0f8f3-112">Przykładowa zmiana liczby partycji i liczby replik usługi wyszukiwania w usłudze Azure to 2.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="0f8f3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f8f3-113">PARAMETERS</span></span>

### <span data-ttu-id="0f8f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f8f3-114">-DefaultProfile</span></span>
<span data-ttu-id="0f8f3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f8f3-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0f8f3-116">-InputObject</span></span>
<span data-ttu-id="0f8f3-117">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="0f8f3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0f8f3-118">-Name</span></span>
<span data-ttu-id="0f8f3-119">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-119">Search Service name.</span></span>

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

### <span data-ttu-id="0f8f3-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="0f8f3-120">-PartitionCount</span></span>
<span data-ttu-id="0f8f3-121">Liczba partycji usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="0f8f3-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="0f8f3-122">-ReplicaCount</span></span>
<span data-ttu-id="0f8f3-123">Liczba replik usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="0f8f3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f8f3-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f8f3-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-125">Resource Group name.</span></span>

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

### <span data-ttu-id="0f8f3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f8f3-126">-ResourceId</span></span>
<span data-ttu-id="0f8f3-127">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="0f8f3-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f8f3-128">-Confirm</span></span>
<span data-ttu-id="0f8f3-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f8f3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f8f3-130">-WhatIf</span></span>
<span data-ttu-id="0f8f3-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f8f3-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f8f3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f8f3-133">CommonParameters</span></span>
<span data-ttu-id="0f8f3-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f8f3-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f8f3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f8f3-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f8f3-136">INPUTS</span></span>

### <span data-ttu-id="0f8f3-137">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="0f8f3-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="0f8f3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0f8f3-138">System.String</span></span>

## <span data-ttu-id="0f8f3-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f8f3-139">OUTPUTS</span></span>

### <span data-ttu-id="0f8f3-140">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="0f8f3-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="0f8f3-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f8f3-141">NOTES</span></span>

## <span data-ttu-id="0f8f3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f8f3-142">RELATED LINKS</span></span>

[<span data-ttu-id="0f8f3-143">Nowe — AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0f8f3-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="0f8f3-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0f8f3-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="0f8f3-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0f8f3-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)