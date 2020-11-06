---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscachediagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: ea99137cdd97963bd3d16c9bf0d9b81012e3352b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552571"
---
# <span data-ttu-id="7a3d0-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7a3d0-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="7a3d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="7a3d0-103">Włącza diagnostykę w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a3d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a3d0-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a3d0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a3d0-105">DESCRIPTION</span></span>
<span data-ttu-id="7a3d0-106">Polecenie cmdlet **Set-AzureRmRedisCacheDiagnostics** włącza diagnostykę pamięci podręcznej usługi Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="7a3d0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a3d0-107">EXAMPLES</span></span>

### <span data-ttu-id="7a3d0-108">Przykład 1: Włączanie diagnostyki</span><span class="sxs-lookup"><span data-stu-id="7a3d0-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="7a3d0-109">To polecenie włącza diagnostykę w pamięci podręcznej usługi Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="7a3d0-110">To polecenie umożliwia diagnostykę lub zaktualizowanie konta magazynu dla wszystkich pamięci podręcznej usługi Azure Redis w tym samym regionie dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="7a3d0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a3d0-111">PARAMETERS</span></span>

### <span data-ttu-id="7a3d0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a3d0-112">-DefaultProfile</span></span>
<span data-ttu-id="7a3d0-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a3d0-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a3d0-114">-Name</span></span>
<span data-ttu-id="7a3d0-115">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="7a3d0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a3d0-116">-ResourceGroupName</span></span>
<span data-ttu-id="7a3d0-117">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="7a3d0-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7a3d0-118">-StorageAccountId</span></span>
<span data-ttu-id="7a3d0-119">Określa identyfikator zasobu konta magazynu służącego do przechowywania danych diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="7a3d0-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a3d0-120">-Confirm</span></span>
<span data-ttu-id="7a3d0-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a3d0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a3d0-122">-WhatIf</span></span>
<span data-ttu-id="7a3d0-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a3d0-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a3d0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a3d0-125">CommonParameters</span></span>
<span data-ttu-id="7a3d0-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a3d0-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a3d0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a3d0-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a3d0-128">INPUTS</span></span>

### <span data-ttu-id="7a3d0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7a3d0-129">System.String</span></span>

## <span data-ttu-id="7a3d0-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a3d0-130">OUTPUTS</span></span>

### <span data-ttu-id="7a3d0-131">System. void</span><span class="sxs-lookup"><span data-stu-id="7a3d0-131">System.Void</span></span>

## <span data-ttu-id="7a3d0-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a3d0-132">NOTES</span></span>
* <span data-ttu-id="7a3d0-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="7a3d0-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="7a3d0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a3d0-134">RELATED LINKS</span></span>

[<span data-ttu-id="7a3d0-135">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7a3d0-135">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)


