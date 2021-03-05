---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 9b1957054c243de8776f0063e236f9e19980af54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982289"
---
# <span data-ttu-id="ca28a-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ca28a-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="ca28a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca28a-102">SYNOPSIS</span></span>
<span data-ttu-id="ca28a-103">Uzyskaj link replikacji geograficznej dla funkcji Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="ca28a-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="ca28a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ca28a-104">SYNTAX</span></span>

### <span data-ttu-id="ca28a-105">AllLinksForCache (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ca28a-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca28a-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="ca28a-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca28a-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="ca28a-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca28a-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="ca28a-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca28a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="ca28a-109">DESCRIPTION</span></span>
<span data-ttu-id="ca28a-110">Istnieją cztery różne sposoby uzyskania szczegółów linku replikacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="ca28a-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="ca28a-111">Podaj nazwę parametru albo parametr PrimaryServerName i/lub SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="ca28a-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="ca28a-112">Zostanie nadana nazwa, a następnie zostanie zwrócony cały link tam, gdzie istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="ca28a-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="ca28a-113">Jeśli zostanie podana tylko nazwa PrimaryServerName, zostaną zwrócone wszystkie linki, dla których jest podstawową pamięcią podręczną.</span><span class="sxs-lookup"><span data-stu-id="ca28a-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="ca28a-114">Jeśli zostanie podana tylko nazwa SecondaryServerName, zostaną zwrócone wszystkie linki, dla których jest zwracana pomocnicza pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="ca28a-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="ca28a-115">Jeśli zarówno nazwa PrimaryServerName, jak i nazwa SecondaryServerName zostaną podane, zostanie zwrócony konkretny link z poprawną rolą.</span><span class="sxs-lookup"><span data-stu-id="ca28a-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="ca28a-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ca28a-116">EXAMPLES</span></span>

### <span data-ttu-id="ca28a-117">Przykład 1. Korzystanie z zestawu parametrów AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="ca28a-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="ca28a-118">To polecenie pobiera wszystkie linki replikacji geograficznej dla funkcji Redis Cache o nazwie mycache1.</span><span class="sxs-lookup"><span data-stu-id="ca28a-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="ca28a-119">Przykład 2. Korzystanie z zestawu parametrów AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="ca28a-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="ca28a-120">To polecenie pobiera linki replikacji geograficznej, których podstawową nazwą jest pamięć podręczna Redis Cache o nazwie mycache1.</span><span class="sxs-lookup"><span data-stu-id="ca28a-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="ca28a-121">Przykład 3. Korzystanie z zestawu parametrów AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="ca28a-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="ca28a-122">To polecenie pobiera linki replikacji geograficznej, gdzie funkcja Redis Cache o nazwie mycache2 jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="ca28a-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="ca28a-123">Przykład 4. Korzystanie z zestawu parametrów SingleLink</span><span class="sxs-lookup"><span data-stu-id="ca28a-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="ca28a-124">To polecenie pobiera pojedyncze linki replikacji geograficznej, gdzie funkcja Redis Cache o nazwie mycache1 jest podstawowa, a funkcja Redis Cache o nazwie mycache2 jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="ca28a-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="ca28a-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca28a-125">PARAMETERS</span></span>

### <span data-ttu-id="ca28a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca28a-126">-DefaultProfile</span></span>
<span data-ttu-id="ca28a-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca28a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca28a-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ca28a-128">-Name</span></span>
<span data-ttu-id="ca28a-129">Nazwa pamięci podręcznej redis.</span><span class="sxs-lookup"><span data-stu-id="ca28a-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="ca28a-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="ca28a-130">-PrimaryServerName</span></span>
<span data-ttu-id="ca28a-131">Nazwa podstawowej pamięci podręcznej redis w linku.</span><span class="sxs-lookup"><span data-stu-id="ca28a-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="ca28a-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="ca28a-132">-SecondaryServerName</span></span>
<span data-ttu-id="ca28a-133">Nazwa pomocniczej pamięci podręcznej redis w linku.</span><span class="sxs-lookup"><span data-stu-id="ca28a-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="ca28a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca28a-134">CommonParameters</span></span>
<span data-ttu-id="ca28a-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca28a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca28a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca28a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca28a-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca28a-137">INPUTS</span></span>

### <span data-ttu-id="ca28a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ca28a-138">System.String</span></span>

## <span data-ttu-id="ca28a-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca28a-139">OUTPUTS</span></span>

### <span data-ttu-id="ca28a-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="ca28a-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="ca28a-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ca28a-141">NOTES</span></span>

## <span data-ttu-id="ca28a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca28a-142">RELATED LINKS</span></span>

[<span data-ttu-id="ca28a-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ca28a-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="ca28a-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ca28a-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="ca28a-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ca28a-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="ca28a-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ca28a-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="ca28a-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ca28a-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="ca28a-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ca28a-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)