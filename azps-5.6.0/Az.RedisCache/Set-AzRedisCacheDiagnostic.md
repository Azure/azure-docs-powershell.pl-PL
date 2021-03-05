---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: ee6e2848325222d86271bfd70705ec7aa855cbb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000890"
---
# <span data-ttu-id="2d4c4-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2d4c4-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="2d4c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d4c4-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4c4-103">Włącza diagnostykę w usłudze Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="2d4c4-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="2d4c4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2d4c4-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d4c4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2d4c4-105">DESCRIPTION</span></span>
<span data-ttu-id="2d4c4-106">Polecenie **cmdlet Set-AzRedisCacheDiagnostic** umożliwia diagnostykę dla pamięci podręcznej Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="2d4c4-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="2d4c4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2d4c4-107">EXAMPLES</span></span>

### <span data-ttu-id="2d4c4-108">Przykład 1. Włączanie diagnostyki</span><span class="sxs-lookup"><span data-stu-id="2d4c4-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="2d4c4-109">To polecenie umożliwia diagnostykę dla pamięci podręcznej Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="2d4c4-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="2d4c4-110">To polecenie włączy diagnostykę lub zaktualizuje konto magazynu dla wszystkich funkcji Azure Redis Caches w tym samym regionie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2d4c4-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="2d4c4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d4c4-111">PARAMETERS</span></span>

### <span data-ttu-id="2d4c4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d4c4-112">-DefaultProfile</span></span>
<span data-ttu-id="2d4c4-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d4c4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d4c4-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2d4c4-114">-Name</span></span>
<span data-ttu-id="2d4c4-115">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="2d4c4-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="2d4c4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d4c4-116">-ResourceGroupName</span></span>
<span data-ttu-id="2d4c4-117">Określa nazwę grupy zasobów, która zawiera pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="2d4c4-117">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4c4-118">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2d4c4-118">-StorageAccountId</span></span>
<span data-ttu-id="2d4c4-119">Określa identyfikator zasobu konta magazynu używanego do przechowywania danych diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="2d4c4-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="2d4c4-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2d4c4-120">-Confirm</span></span>
<span data-ttu-id="2d4c4-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2d4c4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d4c4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d4c4-122">-WhatIf</span></span>
<span data-ttu-id="2d4c4-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d4c4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d4c4-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2d4c4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d4c4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4c4-125">CommonParameters</span></span>
<span data-ttu-id="2d4c4-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d4c4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4c4-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d4c4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4c4-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d4c4-128">INPUTS</span></span>

### <span data-ttu-id="2d4c4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2d4c4-129">System.String</span></span>

## <span data-ttu-id="2d4c4-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d4c4-130">OUTPUTS</span></span>

### <span data-ttu-id="2d4c4-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="2d4c4-131">System.Void</span></span>

## <span data-ttu-id="2d4c4-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2d4c4-132">NOTES</span></span>
* <span data-ttu-id="2d4c4-133">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="2d4c4-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="2d4c4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d4c4-134">RELATED LINKS</span></span>

[<span data-ttu-id="2d4c4-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2d4c4-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


