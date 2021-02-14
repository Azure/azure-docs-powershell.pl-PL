---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 38c72a19e73d87272fb91fb6472a41496658e7d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183794"
---
# <span data-ttu-id="369de-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="369de-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="369de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="369de-102">SYNOPSIS</span></span>
<span data-ttu-id="369de-103">Usuwanie łącza replikacji geograficznej między dwoma pamięciami podręczni redis.</span><span class="sxs-lookup"><span data-stu-id="369de-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="369de-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="369de-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="369de-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="369de-105">DESCRIPTION</span></span>
<span data-ttu-id="369de-106">Usuwanie łącza replikacji geograficznej między dwoma pamięciami podręczni redis.</span><span class="sxs-lookup"><span data-stu-id="369de-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="369de-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="369de-107">EXAMPLES</span></span>

### <span data-ttu-id="369de-108">Przykład 1. Usuwanie linku replikacji geograficznej</span><span class="sxs-lookup"><span data-stu-id="369de-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="369de-109">To polecenie usuwa linki replikacji geograficznej, gdzie funkcja Redis Cache o nazwie mycache1 jest podstawowa, a funkcja Redis Cache o nazwie mycache2 jest pomocnicza.</span><span class="sxs-lookup"><span data-stu-id="369de-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="369de-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="369de-110">PARAMETERS</span></span>

### <span data-ttu-id="369de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="369de-111">-DefaultProfile</span></span>
<span data-ttu-id="369de-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="369de-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="369de-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="369de-113">-PassThru</span></span>
<span data-ttu-id="369de-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="369de-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="369de-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="369de-115">-PrimaryServerName</span></span>
<span data-ttu-id="369de-116">Nazwa podstawowej pamięci podręcznej redis w linku.</span><span class="sxs-lookup"><span data-stu-id="369de-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="369de-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="369de-117">-SecondaryServerName</span></span>
<span data-ttu-id="369de-118">Nazwa pomocniczej pamięci podręcznej redis w linku.</span><span class="sxs-lookup"><span data-stu-id="369de-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="369de-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="369de-119">-Confirm</span></span>
<span data-ttu-id="369de-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="369de-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="369de-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="369de-121">-WhatIf</span></span>
<span data-ttu-id="369de-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="369de-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="369de-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="369de-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="369de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="369de-124">CommonParameters</span></span>
<span data-ttu-id="369de-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="369de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="369de-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="369de-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="369de-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="369de-127">INPUTS</span></span>

### <span data-ttu-id="369de-128">System.String</span><span class="sxs-lookup"><span data-stu-id="369de-128">System.String</span></span>

## <span data-ttu-id="369de-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="369de-129">OUTPUTS</span></span>

### <span data-ttu-id="369de-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="369de-130">System.Boolean</span></span>

## <span data-ttu-id="369de-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="369de-131">NOTES</span></span>

## <span data-ttu-id="369de-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="369de-132">RELATED LINKS</span></span>

[<span data-ttu-id="369de-133">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="369de-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="369de-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="369de-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="369de-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="369de-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="369de-136">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="369de-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="369de-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="369de-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="369de-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="369de-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)