---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052531"
---
# <span data-ttu-id="3a656-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3a656-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="3a656-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a656-102">SYNOPSIS</span></span>
<span data-ttu-id="3a656-103">Uzyskaj link replikacji Geo dla pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="3a656-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="3a656-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a656-104">SYNTAX</span></span>

### <span data-ttu-id="3a656-105">AllLinksForCache (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3a656-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a656-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="3a656-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a656-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="3a656-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a656-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="3a656-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a656-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3a656-109">DESCRIPTION</span></span>
<span data-ttu-id="3a656-110">Istnieją cztery różne sposoby uzyskiwania szczegółów linku replikacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="3a656-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="3a656-111">Podaj nazwę parametru lub PrimaryServerName i/lub SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="3a656-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="3a656-112">Imię i nazwisko, a wszystkie linki, w których istnieje pamięć podręczna, zostaną zwrócone.</span><span class="sxs-lookup"><span data-stu-id="3a656-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="3a656-113">Jeśli jest podany tylko PrimaryServerName, zostaną zwrócone wszystkie linki, w przypadku których pamięć podręczna jest podstawowa.</span><span class="sxs-lookup"><span data-stu-id="3a656-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="3a656-114">Jeśli jest podany tylko SecondaryServerName, zostaną zwrócone wszystkie linki, w których pamięć podręczna jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="3a656-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="3a656-115">Jeśli PrimaryServerName i SecondaryServerName są podane, zostanie zwrócona konkretna wartość linku o odpowiedniej roli.</span><span class="sxs-lookup"><span data-stu-id="3a656-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="3a656-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a656-116">EXAMPLES</span></span>

### <span data-ttu-id="3a656-117">Przykład 1: uzyskiwanie używania zestawu parametrów AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="3a656-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="3a656-118">To polecenie pobiera wszystkie linki replikacji geograficznej dla pamięci podręcznej Redis o nazwie mycache1.</span><span class="sxs-lookup"><span data-stu-id="3a656-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="3a656-119">Przykład 2: uzyskiwanie dostępu za pomocą zestawu parametrów AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="3a656-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="3a656-120">To polecenie pobiera linki replikacji geograficznej, w której Redis pamięć podręczna o nazwie mycache1 to Primary.</span><span class="sxs-lookup"><span data-stu-id="3a656-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="3a656-121">Przykład 3: uzyskiwanie dostępu za pomocą zestawu parametrów AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="3a656-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="3a656-122">To polecenie pobiera linki replikacji geograficznej, w której Redis pamięć podręczna o nazwie mycache2 jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="3a656-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="3a656-123">Przykład 4: uzyskiwanie używania zestawu parametrów SingleLink</span><span class="sxs-lookup"><span data-stu-id="3a656-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="3a656-124">To polecenie pobiera pojedyncze linki replikacji geograficznej, w której pamięć podręczna Redis o nazwie mycache1 jest podstawowa, a pamięć podręczna Redis o nazwie mycache2 jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="3a656-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="3a656-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a656-125">PARAMETERS</span></span>

### <span data-ttu-id="3a656-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a656-126">-DefaultProfile</span></span>
<span data-ttu-id="3a656-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a656-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a656-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a656-128">-Name</span></span>
<span data-ttu-id="3a656-129">Nazwa pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="3a656-129">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a656-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="3a656-130">-PrimaryServerName</span></span>
<span data-ttu-id="3a656-131">Nazwa pamięci podręcznej Redis głównej w łączu.</span><span class="sxs-lookup"><span data-stu-id="3a656-131">Name of primary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a656-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="3a656-132">-SecondaryServerName</span></span>
<span data-ttu-id="3a656-133">Nazwa pomocniczej pamięci podręcznej Redis w łączu.</span><span class="sxs-lookup"><span data-stu-id="3a656-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a656-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a656-134">CommonParameters</span></span>
<span data-ttu-id="3a656-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a656-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a656-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a656-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a656-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a656-137">INPUTS</span></span>

### <span data-ttu-id="3a656-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3a656-138">System.String</span></span>

## <span data-ttu-id="3a656-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a656-139">OUTPUTS</span></span>

### <span data-ttu-id="3a656-140">Microsoft. Azure. Commands. RedisCache. models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="3a656-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="3a656-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a656-141">NOTES</span></span>

## <span data-ttu-id="3a656-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a656-142">RELATED LINKS</span></span>

[<span data-ttu-id="3a656-143">Nowe — AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3a656-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="3a656-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3a656-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="3a656-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a656-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="3a656-146">Nowe — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a656-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="3a656-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a656-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="3a656-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a656-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)