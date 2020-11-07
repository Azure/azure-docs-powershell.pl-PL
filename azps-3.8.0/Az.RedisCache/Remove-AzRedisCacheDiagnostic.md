---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896085"
---
# <span data-ttu-id="3e22f-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3e22f-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="3e22f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e22f-102">SYNOPSIS</span></span>
<span data-ttu-id="3e22f-103">Wyłącza diagnostykę w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="3e22f-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="3e22f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e22f-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e22f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3e22f-105">DESCRIPTION</span></span>
<span data-ttu-id="3e22f-106">Polecenie cmdlet **Remove-AzRedisCacheDiagnostic** wyłącza diagnostykę w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="3e22f-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="3e22f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e22f-107">EXAMPLES</span></span>

### <span data-ttu-id="3e22f-108">Przykład 1: wyłączanie diagnostyki</span><span class="sxs-lookup"><span data-stu-id="3e22f-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="3e22f-109">To polecenie wyłącza diagnostykę w określonej pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="3e22f-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="3e22f-110">Spowoduje to wyłączenie diagnostyki wszystkich pamięci podręcznych usługi Azure Redis w tym samym regionie dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3e22f-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="3e22f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e22f-111">PARAMETERS</span></span>

### <span data-ttu-id="3e22f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e22f-112">-DefaultProfile</span></span>
<span data-ttu-id="3e22f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e22f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e22f-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e22f-114">-Name</span></span>
<span data-ttu-id="3e22f-115">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="3e22f-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="3e22f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e22f-116">-ResourceGroupName</span></span>
<span data-ttu-id="3e22f-117">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="3e22f-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="3e22f-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e22f-118">-Confirm</span></span>
<span data-ttu-id="3e22f-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e22f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e22f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e22f-120">-WhatIf</span></span>
<span data-ttu-id="3e22f-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e22f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e22f-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e22f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e22f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e22f-123">CommonParameters</span></span>
<span data-ttu-id="3e22f-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e22f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e22f-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e22f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e22f-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e22f-126">INPUTS</span></span>

### <span data-ttu-id="3e22f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3e22f-127">System.String</span></span>

## <span data-ttu-id="3e22f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e22f-128">OUTPUTS</span></span>

### <span data-ttu-id="3e22f-129">System. void</span><span class="sxs-lookup"><span data-stu-id="3e22f-129">System.Void</span></span>

## <span data-ttu-id="3e22f-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e22f-130">NOTES</span></span>
* <span data-ttu-id="3e22f-131">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="3e22f-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="3e22f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e22f-132">RELATED LINKS</span></span>

[<span data-ttu-id="3e22f-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3e22f-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


