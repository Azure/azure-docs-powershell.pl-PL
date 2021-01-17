---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 38c72a19e73d87272fb91fb6472a41496658e7d6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490709"
---
# <span data-ttu-id="08c4d-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="08c4d-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="08c4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="08c4d-103">Usuń łącze replikacji Geo między dwiema Redis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="08c4d-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="08c4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08c4d-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08c4d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="08c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="08c4d-106">Usuń łącze replikacji Geo między dwiema Redis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="08c4d-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="08c4d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08c4d-107">EXAMPLES</span></span>

### <span data-ttu-id="08c4d-108">Przykład 1: usuwanie linku replikacji Geo</span><span class="sxs-lookup"><span data-stu-id="08c4d-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="08c4d-109">To polecenie usuwa linki replikacji geograficznej, w której pamięć podręczna Redis o nazwie mycache1 jest podstawowa, a pamięć podręczna Redis o nazwie mycache2 jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="08c4d-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="08c4d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08c4d-110">PARAMETERS</span></span>

### <span data-ttu-id="08c4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c4d-111">-DefaultProfile</span></span>
<span data-ttu-id="08c4d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08c4d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08c4d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08c4d-113">-PassThru</span></span>
<span data-ttu-id="08c4d-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="08c4d-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="08c4d-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="08c4d-115">-PrimaryServerName</span></span>
<span data-ttu-id="08c4d-116">Nazwa pamięci podręcznej Redis głównej w łączu.</span><span class="sxs-lookup"><span data-stu-id="08c4d-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="08c4d-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="08c4d-117">-SecondaryServerName</span></span>
<span data-ttu-id="08c4d-118">Nazwa pomocniczej pamięci podręcznej Redis w łączu.</span><span class="sxs-lookup"><span data-stu-id="08c4d-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="08c4d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08c4d-119">-Confirm</span></span>
<span data-ttu-id="08c4d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08c4d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08c4d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08c4d-121">-WhatIf</span></span>
<span data-ttu-id="08c4d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08c4d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08c4d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08c4d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08c4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c4d-124">CommonParameters</span></span>
<span data-ttu-id="08c4d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08c4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c4d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08c4d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c4d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08c4d-127">INPUTS</span></span>

### <span data-ttu-id="08c4d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="08c4d-128">System.String</span></span>

## <span data-ttu-id="08c4d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08c4d-129">OUTPUTS</span></span>

### <span data-ttu-id="08c4d-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08c4d-130">System.Boolean</span></span>

## <span data-ttu-id="08c4d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08c4d-131">NOTES</span></span>

## <span data-ttu-id="08c4d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08c4d-132">RELATED LINKS</span></span>

[<span data-ttu-id="08c4d-133">Nowe — AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="08c4d-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="08c4d-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="08c4d-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="08c4d-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08c4d-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="08c4d-136">Nowe — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08c4d-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="08c4d-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08c4d-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="08c4d-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08c4d-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)