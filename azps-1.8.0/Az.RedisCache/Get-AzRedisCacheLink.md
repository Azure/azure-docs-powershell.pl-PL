---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 8129634e940624fe09dad4a1199f96dbcf5162bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708524"
---
# <span data-ttu-id="168b8-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="168b8-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="168b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="168b8-102">SYNOPSIS</span></span>
<span data-ttu-id="168b8-103">Uzyskaj link replikacji Geo dla pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="168b8-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="168b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="168b8-104">SYNTAX</span></span>

### <span data-ttu-id="168b8-105">AllLinksForCache (domyślny)</span><span class="sxs-lookup"><span data-stu-id="168b8-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="168b8-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="168b8-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="168b8-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="168b8-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="168b8-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="168b8-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="168b8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="168b8-109">DESCRIPTION</span></span>
<span data-ttu-id="168b8-110">Istnieją cztery różne sposoby uzyskiwania szczegółów linku replikacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="168b8-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="168b8-111">Podaj nazwę parametru lub PrimaryServerName i/lub SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="168b8-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="168b8-112">Imię i nazwisko, a wszystkie linki, w których istnieje pamięć podręczna, zostaną zwrócone.</span><span class="sxs-lookup"><span data-stu-id="168b8-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="168b8-113">Jeśli jest podany tylko PrimaryServerName, zostaną zwrócone wszystkie linki, w przypadku których pamięć podręczna jest podstawowa.</span><span class="sxs-lookup"><span data-stu-id="168b8-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="168b8-114">Jeśli jest podany tylko SecondaryServerName, zostaną zwrócone wszystkie linki, w których pamięć podręczna jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="168b8-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="168b8-115">Jeśli PrimaryServerName i SecondaryServerName są podane, zostanie zwrócona konkretna wartość linku o odpowiedniej roli.</span><span class="sxs-lookup"><span data-stu-id="168b8-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="168b8-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="168b8-116">EXAMPLES</span></span>

### <span data-ttu-id="168b8-117">Przykład 1: uzyskiwanie używania zestawu parametrów AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="168b8-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="168b8-118">To polecenie pobiera wszystkie linki replikacji geograficznej dla pamięci podręcznej Redis o nazwie mycache1.</span><span class="sxs-lookup"><span data-stu-id="168b8-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="168b8-119">Przykład 2: uzyskiwanie dostępu za pomocą zestawu parametrów AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="168b8-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="168b8-120">To polecenie pobiera linki replikacji geograficznej, w której Redis pamięć podręczna o nazwie mycache1 to Primary.</span><span class="sxs-lookup"><span data-stu-id="168b8-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="168b8-121">Przykład 3: uzyskiwanie dostępu za pomocą zestawu parametrów AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="168b8-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="168b8-122">To polecenie pobiera linki replikacji geograficznej, w której Redis pamięć podręczna o nazwie mycache2 jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="168b8-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="168b8-123">Przykład 4: uzyskiwanie używania zestawu parametrów SingleLink</span><span class="sxs-lookup"><span data-stu-id="168b8-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="168b8-124">To polecenie pobiera pojedyncze linki replikacji geograficznej, w której pamięć podręczna Redis o nazwie mycache1 jest podstawowa, a pamięć podręczna Redis o nazwie mycache2 jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="168b8-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="168b8-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="168b8-125">PARAMETERS</span></span>

### <span data-ttu-id="168b8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="168b8-126">-DefaultProfile</span></span>
<span data-ttu-id="168b8-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="168b8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="168b8-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="168b8-128">-Name</span></span>
<span data-ttu-id="168b8-129">Nazwa pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="168b8-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="168b8-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="168b8-130">-PrimaryServerName</span></span>
<span data-ttu-id="168b8-131">Nazwa pamięci podręcznej Redis głównej w łączu.</span><span class="sxs-lookup"><span data-stu-id="168b8-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="168b8-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="168b8-132">-SecondaryServerName</span></span>
<span data-ttu-id="168b8-133">Nazwa pomocniczej pamięci podręcznej Redis w łączu.</span><span class="sxs-lookup"><span data-stu-id="168b8-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="168b8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="168b8-134">CommonParameters</span></span>
<span data-ttu-id="168b8-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="168b8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="168b8-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="168b8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="168b8-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="168b8-137">INPUTS</span></span>

### <span data-ttu-id="168b8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="168b8-138">System.String</span></span>

## <span data-ttu-id="168b8-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="168b8-139">OUTPUTS</span></span>

### <span data-ttu-id="168b8-140">Microsoft. Azure. Commands. RedisCache. models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="168b8-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="168b8-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="168b8-141">NOTES</span></span>

## <span data-ttu-id="168b8-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="168b8-142">RELATED LINKS</span></span>

[<span data-ttu-id="168b8-143">Nowe — AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="168b8-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="168b8-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="168b8-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="168b8-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="168b8-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="168b8-146">Nowe — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="168b8-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="168b8-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="168b8-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="168b8-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="168b8-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)