---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: a45407fc7f25e2c7bee5c591ab3110b0620a2c0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544892"
---
# <span data-ttu-id="2ab76-101">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2ab76-101">Get-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="2ab76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ab76-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab76-103">Uzyskaj link replikacji Geo dla pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="2ab76-103">Get geo replication link for Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ab76-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ab76-104">SYNTAX</span></span>

### <span data-ttu-id="2ab76-105">AllLinksForCache (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2ab76-105">AllLinksForCache (Default)</span></span>
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ab76-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="2ab76-106">AllLinksForPrimaryCache</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ab76-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="2ab76-107">SingleLink</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ab76-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="2ab76-108">AllLinksForSecondaryCache</span></span>
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ab76-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2ab76-109">DESCRIPTION</span></span>
<span data-ttu-id="2ab76-110">Istnieją cztery różne sposoby uzyskiwania szczegółów linku replikacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="2ab76-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="2ab76-111">Podaj nazwę parametru lub PrimaryServerName i/lub SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="2ab76-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="2ab76-112">Imię i nazwisko, a wszystkie linki, w których istnieje pamięć podręczna, zostaną zwrócone.</span><span class="sxs-lookup"><span data-stu-id="2ab76-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="2ab76-113">Jeśli jest podany tylko PrimaryServerName, zostaną zwrócone wszystkie linki, w przypadku których pamięć podręczna jest podstawowa.</span><span class="sxs-lookup"><span data-stu-id="2ab76-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="2ab76-114">Jeśli jest podany tylko SecondaryServerName, zostaną zwrócone wszystkie linki, w których pamięć podręczna jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="2ab76-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="2ab76-115">Jeśli PrimaryServerName i SecondaryServerName są podane, zostanie zwrócona konkretna wartość linku o odpowiedniej roli.</span><span class="sxs-lookup"><span data-stu-id="2ab76-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="2ab76-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ab76-116">EXAMPLES</span></span>

### <span data-ttu-id="2ab76-117">Przykład 1: uzyskiwanie używania zestawu parametrów AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="2ab76-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="2ab76-118">To polecenie pobiera wszystkie linki replikacji geograficznej dla pamięci podręcznej Redis o nazwie mycache1.</span><span class="sxs-lookup"><span data-stu-id="2ab76-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="2ab76-119">Przykład 2: uzyskiwanie dostępu za pomocą zestawu parametrów AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="2ab76-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="2ab76-120">To polecenie pobiera linki replikacji geograficznej, w której Redis pamięć podręczna o nazwie mycache1 to Primary.</span><span class="sxs-lookup"><span data-stu-id="2ab76-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="2ab76-121">Przykład 3: uzyskiwanie dostępu za pomocą zestawu parametrów AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="2ab76-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="2ab76-122">To polecenie pobiera linki replikacji geograficznej, w której Redis pamięć podręczna o nazwie mycache2 jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="2ab76-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="2ab76-123">Przykład 4: uzyskiwanie używania zestawu parametrów SingleLink</span><span class="sxs-lookup"><span data-stu-id="2ab76-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="2ab76-124">To polecenie pobiera pojedyncze linki replikacji geograficznej, w której pamięć podręczna Redis o nazwie mycache1 jest podstawowa, a pamięć podręczna Redis o nazwie mycache2 jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="2ab76-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="2ab76-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ab76-125">PARAMETERS</span></span>

### <span data-ttu-id="2ab76-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab76-126">-DefaultProfile</span></span>
<span data-ttu-id="2ab76-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab76-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ab76-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2ab76-128">-Name</span></span>
<span data-ttu-id="2ab76-129">Nazwa pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="2ab76-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="2ab76-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="2ab76-130">-PrimaryServerName</span></span>
<span data-ttu-id="2ab76-131">Nazwa pamięci podręcznej Redis głównej w łączu.</span><span class="sxs-lookup"><span data-stu-id="2ab76-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="2ab76-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="2ab76-132">-SecondaryServerName</span></span>
<span data-ttu-id="2ab76-133">Nazwa pomocniczej pamięci podręcznej Redis w łączu.</span><span class="sxs-lookup"><span data-stu-id="2ab76-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="2ab76-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab76-134">CommonParameters</span></span>
<span data-ttu-id="2ab76-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ab76-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab76-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ab76-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab76-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ab76-137">INPUTS</span></span>

### <span data-ttu-id="2ab76-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2ab76-138">System.String</span></span>

## <span data-ttu-id="2ab76-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ab76-139">OUTPUTS</span></span>

### <span data-ttu-id="2ab76-140">Microsoft. Azure. Commands. RedisCache. models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="2ab76-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="2ab76-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ab76-141">NOTES</span></span>

## <span data-ttu-id="2ab76-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ab76-142">RELATED LINKS</span></span>

[<span data-ttu-id="2ab76-143">Nowe — AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2ab76-143">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="2ab76-144">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2ab76-144">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="2ab76-145">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2ab76-145">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="2ab76-146">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2ab76-146">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="2ab76-147">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2ab76-147">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="2ab76-148">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2ab76-148">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
