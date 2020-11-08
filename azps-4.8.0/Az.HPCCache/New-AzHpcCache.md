---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221186"
---
# <span data-ttu-id="a5b82-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="a5b82-101">New-AzHpcCache</span></span>

## <span data-ttu-id="a5b82-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5b82-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b82-103">Tworzy pamięć podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="a5b82-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="a5b82-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5b82-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5b82-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a5b82-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b82-106">Polecenie cmdlet **New-AzHpcCache** tworzy pamięć podręczną usługi Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="a5b82-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="a5b82-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5b82-107">EXAMPLES</span></span>

### <span data-ttu-id="a5b82-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5b82-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="a5b82-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5b82-109">PARAMETERS</span></span>

### <span data-ttu-id="a5b82-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5b82-110">-AsJob</span></span>
<span data-ttu-id="a5b82-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a5b82-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5b82-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="a5b82-112">-CacheSize</span></span>
<span data-ttu-id="a5b82-113">CacheSize.</span><span class="sxs-lookup"><span data-stu-id="a5b82-113">CacheSize.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b82-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b82-114">-DefaultProfile</span></span>
<span data-ttu-id="a5b82-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b82-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b82-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a5b82-116">-Location</span></span>
<span data-ttu-id="a5b82-117">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="a5b82-117">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b82-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5b82-118">-Name</span></span>
<span data-ttu-id="a5b82-119">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="a5b82-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b82-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b82-120">-ResourceGroupName</span></span>
<span data-ttu-id="a5b82-121">Nazwa grupy zasobów, w której ma zostać utworzona pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="a5b82-121">Name of resource group under which you want to create cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b82-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="a5b82-122">-Sku</span></span>
<span data-ttu-id="a5b82-123">Zapas.</span><span class="sxs-lookup"><span data-stu-id="a5b82-123">Sku.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b82-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="a5b82-124">-SubnetUri</span></span>
<span data-ttu-id="a5b82-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="a5b82-125">SubnetURI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b82-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5b82-126">-Tag</span></span>
<span data-ttu-id="a5b82-127">Znaczniki, które mają zostać skojarzone z pamięcią podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="a5b82-127">The tags to associate with HPC Cache.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b82-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5b82-128">-Confirm</span></span>
<span data-ttu-id="a5b82-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5b82-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b82-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b82-130">-WhatIf</span></span>
<span data-ttu-id="a5b82-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5b82-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5b82-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a5b82-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b82-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b82-133">CommonParameters</span></span>
<span data-ttu-id="a5b82-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b82-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b82-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5b82-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b82-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5b82-136">INPUTS</span></span>

### <span data-ttu-id="a5b82-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a5b82-137">System.String</span></span>

### <span data-ttu-id="a5b82-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a5b82-138">System.Int32</span></span>

## <span data-ttu-id="a5b82-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5b82-139">OUTPUTS</span></span>

### <span data-ttu-id="a5b82-140">Microsoft. Azure. PowerShell. polecenia. HPCCache. models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="a5b82-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="a5b82-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5b82-141">NOTES</span></span>

## <span data-ttu-id="a5b82-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5b82-142">RELATED LINKS</span></span>
