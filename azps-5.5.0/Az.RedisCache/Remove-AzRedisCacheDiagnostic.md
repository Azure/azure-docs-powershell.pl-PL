---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240186"
---
# <span data-ttu-id="43d1d-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="43d1d-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="43d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="43d1d-103">Wyłącza diagnostykę w usłudze Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="43d1d-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="43d1d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="43d1d-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43d1d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="43d1d-105">DESCRIPTION</span></span>
<span data-ttu-id="43d1d-106">Polecenie **cmdlet Remove-AzRedisCacheDiagnostic** wyłącza diagnostykę w usłudze Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="43d1d-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="43d1d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="43d1d-107">EXAMPLES</span></span>

### <span data-ttu-id="43d1d-108">Przykład 1. Wyłączanie diagnostyki</span><span class="sxs-lookup"><span data-stu-id="43d1d-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="43d1d-109">To polecenie wyłącza diagnostykę w określonej usłudze Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="43d1d-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="43d1d-110">Spowoduje to wyłączenie diagnostyki dla wszystkich funkcji Azure Redis Cache w tym samym regionie dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="43d1d-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="43d1d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43d1d-111">PARAMETERS</span></span>

### <span data-ttu-id="43d1d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d1d-112">-DefaultProfile</span></span>
<span data-ttu-id="43d1d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="43d1d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43d1d-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="43d1d-114">-Name</span></span>
<span data-ttu-id="43d1d-115">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="43d1d-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="43d1d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d1d-116">-ResourceGroupName</span></span>
<span data-ttu-id="43d1d-117">Określa nazwę grupy zasobów, która zawiera pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="43d1d-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="43d1d-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43d1d-118">-Confirm</span></span>
<span data-ttu-id="43d1d-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="43d1d-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d1d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43d1d-120">-WhatIf</span></span>
<span data-ttu-id="43d1d-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43d1d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43d1d-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="43d1d-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d1d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d1d-123">CommonParameters</span></span>
<span data-ttu-id="43d1d-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d1d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d1d-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43d1d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d1d-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43d1d-126">INPUTS</span></span>

### <span data-ttu-id="43d1d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="43d1d-127">System.String</span></span>

## <span data-ttu-id="43d1d-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43d1d-128">OUTPUTS</span></span>

### <span data-ttu-id="43d1d-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="43d1d-129">System.Void</span></span>

## <span data-ttu-id="43d1d-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="43d1d-130">NOTES</span></span>
* <span data-ttu-id="43d1d-131">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="43d1d-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="43d1d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43d1d-132">RELATED LINKS</span></span>

[<span data-ttu-id="43d1d-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="43d1d-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


