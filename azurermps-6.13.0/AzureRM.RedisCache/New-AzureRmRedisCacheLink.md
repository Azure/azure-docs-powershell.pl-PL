---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
ms.openlocfilehash: f625c9180287166b01607c468c44b5e0623c11cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524305"
---
# <span data-ttu-id="68ae6-101">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="68ae6-101">New-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="68ae6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="68ae6-103">Utwórz łącze replikacji geograficznej między dwiema Redis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="68ae6-103">Create a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68ae6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68ae6-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68ae6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="68ae6-105">DESCRIPTION</span></span>
<span data-ttu-id="68ae6-106">Utwórz łącze replikacji geograficznej między dwiema Redis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="68ae6-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="68ae6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68ae6-107">EXAMPLES</span></span>

### <span data-ttu-id="68ae6-108">Przykład 1. Tworzenie łącza między dwiema buforami</span><span class="sxs-lookup"><span data-stu-id="68ae6-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="68ae6-109">To polecenie tworzy link replikacji geograficznej między Redis Cache mycache1 i mycache2.</span><span class="sxs-lookup"><span data-stu-id="68ae6-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="68ae6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68ae6-110">PARAMETERS</span></span>

### <span data-ttu-id="68ae6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ae6-111">-DefaultProfile</span></span>
<span data-ttu-id="68ae6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68ae6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68ae6-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="68ae6-113">-PrimaryServerName</span></span>
<span data-ttu-id="68ae6-114">Nazwa pamięci podręcznej Redis głównej w łączu.</span><span class="sxs-lookup"><span data-stu-id="68ae6-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="68ae6-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="68ae6-115">-SecondaryServerName</span></span>
<span data-ttu-id="68ae6-116">Nazwa pomocniczej pamięci podręcznej Redis w łączu.</span><span class="sxs-lookup"><span data-stu-id="68ae6-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="68ae6-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68ae6-117">-Confirm</span></span>
<span data-ttu-id="68ae6-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68ae6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ae6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ae6-119">-WhatIf</span></span>
<span data-ttu-id="68ae6-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68ae6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68ae6-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68ae6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ae6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ae6-122">CommonParameters</span></span>
<span data-ttu-id="68ae6-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68ae6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ae6-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68ae6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ae6-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68ae6-125">INPUTS</span></span>

### <span data-ttu-id="68ae6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="68ae6-126">System.String</span></span>

## <span data-ttu-id="68ae6-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68ae6-127">OUTPUTS</span></span>

### <span data-ttu-id="68ae6-128">Microsoft. Azure. Commands. RedisCache. models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="68ae6-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="68ae6-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68ae6-129">NOTES</span></span>

## <span data-ttu-id="68ae6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68ae6-130">RELATED LINKS</span></span>

[<span data-ttu-id="68ae6-131">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="68ae6-131">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="68ae6-132">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="68ae6-132">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="68ae6-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="68ae6-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="68ae6-134">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="68ae6-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="68ae6-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="68ae6-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="68ae6-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="68ae6-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
