---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: dff5f565e27f89360465ede3eb8fbe2c3d5620a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542392"
---
# <span data-ttu-id="142b5-101">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="142b5-101">Get-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="142b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="142b5-102">SYNOPSIS</span></span>
<span data-ttu-id="142b5-103">Uzyskaj link replikacji Geo dla pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="142b5-103">Get geo replication link for Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="142b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="142b5-104">SYNTAX</span></span>

### <span data-ttu-id="142b5-105">AllLinksForCache (domyślny)</span><span class="sxs-lookup"><span data-stu-id="142b5-105">AllLinksForCache (Default)</span></span>
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="142b5-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="142b5-106">AllLinksForPrimaryCache</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="142b5-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="142b5-107">SingleLink</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="142b5-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="142b5-108">AllLinksForSecondaryCache</span></span>
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="142b5-109">Opis</span><span class="sxs-lookup"><span data-stu-id="142b5-109">DESCRIPTION</span></span>
<span data-ttu-id="142b5-110">Istnieją cztery różne sposoby uzyskiwania szczegółów linku replikacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="142b5-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="142b5-111">Podaj nazwę parametru lub PrimaryServerName i/lub SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="142b5-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="142b5-112">Imię i nazwisko, a wszystkie linki, w których istnieje pamięć podręczna, zostaną zwrócone.</span><span class="sxs-lookup"><span data-stu-id="142b5-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="142b5-113">Jeśli jest podany tylko PrimaryServerName, zostaną zwrócone wszystkie linki, w przypadku których pamięć podręczna jest podstawowa.</span><span class="sxs-lookup"><span data-stu-id="142b5-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="142b5-114">Jeśli jest podany tylko SecondaryServerName, zostaną zwrócone wszystkie linki, w których pamięć podręczna jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="142b5-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="142b5-115">Jeśli PrimaryServerName i SecondaryServerName są podane, zostanie zwrócona konkretna wartość linku o odpowiedniej roli.</span><span class="sxs-lookup"><span data-stu-id="142b5-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="142b5-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="142b5-116">EXAMPLES</span></span>

### <span data-ttu-id="142b5-117">Przykład 1: uzyskiwanie używania zestawu parametrów AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="142b5-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="142b5-118">To polecenie pobiera wszystkie linki replikacji geograficznej dla pamięci podręcznej Redis o nazwie mycache1.</span><span class="sxs-lookup"><span data-stu-id="142b5-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="142b5-119">Przykład 2: uzyskiwanie dostępu za pomocą zestawu parametrów AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="142b5-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="142b5-120">To polecenie pobiera linki replikacji geograficznej, w której Redis pamięć podręczna o nazwie mycache1 to Primary.</span><span class="sxs-lookup"><span data-stu-id="142b5-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="142b5-121">Przykład 3: uzyskiwanie dostępu za pomocą zestawu parametrów AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="142b5-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="142b5-122">To polecenie pobiera linki replikacji geograficznej, w której Redis pamięć podręczna o nazwie mycache2 jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="142b5-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="142b5-123">Przykład 4: uzyskiwanie używania zestawu parametrów SingleLink</span><span class="sxs-lookup"><span data-stu-id="142b5-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="142b5-124">To polecenie pobiera pojedyncze linki replikacji geograficznej, w której pamięć podręczna Redis o nazwie mycache1 jest podstawowa, a pamięć podręczna Redis o nazwie mycache2 jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="142b5-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="142b5-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="142b5-125">PARAMETERS</span></span>

### <span data-ttu-id="142b5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="142b5-126">-DefaultProfile</span></span>
<span data-ttu-id="142b5-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="142b5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="142b5-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="142b5-128">-Name</span></span>
<span data-ttu-id="142b5-129">Nazwa pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="142b5-129">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="142b5-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="142b5-130">-PrimaryServerName</span></span>
<span data-ttu-id="142b5-131">Nazwa pamięci podręcznej Redis głównej w łączu.</span><span class="sxs-lookup"><span data-stu-id="142b5-131">Name of primary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="142b5-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="142b5-132">-SecondaryServerName</span></span>
<span data-ttu-id="142b5-133">Nazwa pomocniczej pamięci podręcznej Redis w łączu.</span><span class="sxs-lookup"><span data-stu-id="142b5-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="142b5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="142b5-134">CommonParameters</span></span>
<span data-ttu-id="142b5-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="142b5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="142b5-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="142b5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="142b5-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="142b5-137">INPUTS</span></span>

### <span data-ttu-id="142b5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="142b5-138">System.String</span></span>
<span data-ttu-id="142b5-139">Możesz popotokować dane wejściowe tego polecenia cmdlet za pomocą nazwy, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="142b5-139">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="142b5-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="142b5-140">OUTPUTS</span></span>

### <span data-ttu-id="142b5-141">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. RedisCache. MODELES. PSRedisLinkedServer, Microsoft. Azure. Commands. RedisCache, Version = 4.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="142b5-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="142b5-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="142b5-142">NOTES</span></span>

## <span data-ttu-id="142b5-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="142b5-143">RELATED LINKS</span></span>

[<span data-ttu-id="142b5-144">Nowe — AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="142b5-144">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="142b5-145">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="142b5-145">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="142b5-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="142b5-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="142b5-147">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="142b5-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="142b5-148">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="142b5-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="142b5-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="142b5-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
