---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: 157490da6abeae7e947c22e88301d29043722a86
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886545"
---
# <span data-ttu-id="bf5a7-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="bf5a7-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="bf5a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5a7-103">Utwórz łącze replikacji geograficznej między dwiema Redis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="bf5a7-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="bf5a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf5a7-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf5a7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf5a7-105">DESCRIPTION</span></span>
<span data-ttu-id="bf5a7-106">Utwórz łącze replikacji geograficznej między dwiema Redis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="bf5a7-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="bf5a7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf5a7-107">EXAMPLES</span></span>

### <span data-ttu-id="bf5a7-108">Przykład 1. Tworzenie łącza między dwiema buforami</span><span class="sxs-lookup"><span data-stu-id="bf5a7-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="bf5a7-109">To polecenie tworzy link replikacji geograficznej między Redis Cache mycache1 i mycache2.</span><span class="sxs-lookup"><span data-stu-id="bf5a7-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="bf5a7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf5a7-110">PARAMETERS</span></span>

### <span data-ttu-id="bf5a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf5a7-111">-DefaultProfile</span></span>
<span data-ttu-id="bf5a7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf5a7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf5a7-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="bf5a7-113">-PrimaryServerName</span></span>
<span data-ttu-id="bf5a7-114">Nazwa pamięci podręcznej Redis głównej w łączu.</span><span class="sxs-lookup"><span data-stu-id="bf5a7-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="bf5a7-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="bf5a7-115">-SecondaryServerName</span></span>
<span data-ttu-id="bf5a7-116">Nazwa pomocniczej pamięci podręcznej Redis w łączu.</span><span class="sxs-lookup"><span data-stu-id="bf5a7-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="bf5a7-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf5a7-117">-Confirm</span></span>
<span data-ttu-id="bf5a7-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf5a7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf5a7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf5a7-119">-WhatIf</span></span>
<span data-ttu-id="bf5a7-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf5a7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf5a7-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bf5a7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf5a7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5a7-122">CommonParameters</span></span>
<span data-ttu-id="bf5a7-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf5a7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5a7-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf5a7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5a7-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf5a7-125">INPUTS</span></span>

### <span data-ttu-id="bf5a7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bf5a7-126">System.String</span></span>

## <span data-ttu-id="bf5a7-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf5a7-127">OUTPUTS</span></span>

### <span data-ttu-id="bf5a7-128">Microsoft. Azure. Commands. RedisCache. models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="bf5a7-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="bf5a7-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf5a7-129">NOTES</span></span>

## <span data-ttu-id="bf5a7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf5a7-130">RELATED LINKS</span></span>

[<span data-ttu-id="bf5a7-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="bf5a7-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="bf5a7-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="bf5a7-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="bf5a7-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bf5a7-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="bf5a7-134">Nowe — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bf5a7-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="bf5a7-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bf5a7-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="bf5a7-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bf5a7-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)