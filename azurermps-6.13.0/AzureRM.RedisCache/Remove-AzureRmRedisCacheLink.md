---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
ms.openlocfilehash: e4c45095dba8ec72e00fa26eee2d8a3fb6f029fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718594"
---
# <span data-ttu-id="3c64b-101">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3c64b-101">Remove-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="3c64b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c64b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c64b-103">Usuń łącze replikacji Geo między dwiema Redis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="3c64b-103">Remove a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c64b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c64b-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c64b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3c64b-105">DESCRIPTION</span></span>
<span data-ttu-id="3c64b-106">Usuń łącze replikacji Geo między dwiema Redis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="3c64b-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="3c64b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c64b-107">EXAMPLES</span></span>

### <span data-ttu-id="3c64b-108">Przykład 1: usuwanie linku replikacji Geo</span><span class="sxs-lookup"><span data-stu-id="3c64b-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="3c64b-109">To polecenie usuwa linki replikacji geograficznej, w której pamięć podręczna Redis o nazwie mycache1 jest podstawowa, a pamięć podręczna Redis o nazwie mycache2 jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="3c64b-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="3c64b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c64b-110">PARAMETERS</span></span>

### <span data-ttu-id="3c64b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c64b-111">-DefaultProfile</span></span>
<span data-ttu-id="3c64b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c64b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c64b-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c64b-113">-PassThru</span></span>
<span data-ttu-id="3c64b-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3c64b-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3c64b-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="3c64b-115">-PrimaryServerName</span></span>
<span data-ttu-id="3c64b-116">Nazwa pamięci podręcznej Redis głównej w łączu.</span><span class="sxs-lookup"><span data-stu-id="3c64b-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="3c64b-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="3c64b-117">-SecondaryServerName</span></span>
<span data-ttu-id="3c64b-118">Nazwa pomocniczej pamięci podręcznej Redis w łączu.</span><span class="sxs-lookup"><span data-stu-id="3c64b-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="3c64b-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c64b-119">-Confirm</span></span>
<span data-ttu-id="3c64b-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c64b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c64b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c64b-121">-WhatIf</span></span>
<span data-ttu-id="3c64b-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c64b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c64b-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3c64b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c64b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c64b-124">CommonParameters</span></span>
<span data-ttu-id="3c64b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c64b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c64b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c64b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c64b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c64b-127">INPUTS</span></span>

### <span data-ttu-id="3c64b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3c64b-128">System.String</span></span>

## <span data-ttu-id="3c64b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c64b-129">OUTPUTS</span></span>

### <span data-ttu-id="3c64b-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c64b-130">System.Boolean</span></span>

## <span data-ttu-id="3c64b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c64b-131">NOTES</span></span>

## <span data-ttu-id="3c64b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c64b-132">RELATED LINKS</span></span>

[<span data-ttu-id="3c64b-133">Nowe — AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3c64b-133">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="3c64b-134">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3c64b-134">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="3c64b-135">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3c64b-135">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="3c64b-136">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3c64b-136">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="3c64b-137">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3c64b-137">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="3c64b-138">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3c64b-138">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
