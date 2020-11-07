---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
ms.openlocfilehash: dd9e070a0228cf9bc492f8680917ae0f308e9019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718026"
---
# <span data-ttu-id="c8758-101">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="c8758-101">New-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="c8758-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8758-102">SYNOPSIS</span></span>
<span data-ttu-id="c8758-103">Utwórz łącze replikacji geograficznej między dwiema Redis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="c8758-103">Create a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8758-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8758-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8758-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8758-105">DESCRIPTION</span></span>
<span data-ttu-id="c8758-106">Utwórz łącze replikacji geograficznej między dwiema Redis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="c8758-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="c8758-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8758-107">EXAMPLES</span></span>

### <span data-ttu-id="c8758-108">Przykład 1. Tworzenie łącza między dwiema buforami</span><span class="sxs-lookup"><span data-stu-id="c8758-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="c8758-109">To polecenie tworzy link replikacji geograficznej między Redis Cache mycache1 i mycache2.</span><span class="sxs-lookup"><span data-stu-id="c8758-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="c8758-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8758-110">PARAMETERS</span></span>

### <span data-ttu-id="c8758-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8758-111">-DefaultProfile</span></span>
<span data-ttu-id="c8758-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8758-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8758-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="c8758-113">-PrimaryServerName</span></span>
<span data-ttu-id="c8758-114">Nazwa pamięci podręcznej Redis głównej w łączu.</span><span class="sxs-lookup"><span data-stu-id="c8758-114">Name of primary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8758-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="c8758-115">-SecondaryServerName</span></span>
<span data-ttu-id="c8758-116">Nazwa pomocniczej pamięci podręcznej Redis w łączu.</span><span class="sxs-lookup"><span data-stu-id="c8758-116">Name of secondary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8758-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8758-117">-Confirm</span></span>
<span data-ttu-id="c8758-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8758-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8758-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8758-119">-WhatIf</span></span>
<span data-ttu-id="c8758-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8758-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8758-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c8758-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8758-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8758-122">CommonParameters</span></span>
<span data-ttu-id="c8758-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8758-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8758-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8758-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8758-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8758-125">INPUTS</span></span>

### <span data-ttu-id="c8758-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c8758-126">System.String</span></span>

## <span data-ttu-id="c8758-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8758-127">OUTPUTS</span></span>

### <span data-ttu-id="c8758-128">Microsoft. Azure. Commands. RedisCache. models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="c8758-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="c8758-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8758-129">NOTES</span></span>

## <span data-ttu-id="c8758-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8758-130">RELATED LINKS</span></span>

[<span data-ttu-id="c8758-131">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="c8758-131">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="c8758-132">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="c8758-132">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="c8758-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c8758-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="c8758-134">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c8758-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="c8758-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c8758-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="c8758-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c8758-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
