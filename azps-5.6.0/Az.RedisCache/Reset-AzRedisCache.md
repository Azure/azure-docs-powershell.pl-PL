---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: 797ea800962e00dfd94e1be14e39293fc303ef38
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000922"
---
# <span data-ttu-id="6fd34-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd34-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="6fd34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fd34-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd34-103">Powoduje ponowne uruchomienie węzłów pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="6fd34-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="6fd34-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6fd34-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fd34-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6fd34-105">DESCRIPTION</span></span>
<span data-ttu-id="6fd34-106">Polecenie **cmdlet Reset-AzRedisCache** powoduje ponowne uruchomienie węzłów wystąpienia usługi Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="6fd34-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="6fd34-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6fd34-107">EXAMPLES</span></span>

### <span data-ttu-id="6fd34-108">Przykład 1. Ponowne uruchomienie obu węzłów</span><span class="sxs-lookup"><span data-stu-id="6fd34-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="6fd34-109">To polecenie powoduje ponowne uruchomienie obu węzłów dla pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="6fd34-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="6fd34-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fd34-110">PARAMETERS</span></span>

### <span data-ttu-id="6fd34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd34-111">-DefaultProfile</span></span>
<span data-ttu-id="6fd34-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd34-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fd34-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6fd34-113">-Force</span></span>
<span data-ttu-id="6fd34-114">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6fd34-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6fd34-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6fd34-115">-Name</span></span>
<span data-ttu-id="6fd34-116">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="6fd34-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="6fd34-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fd34-117">-PassThru</span></span>
<span data-ttu-id="6fd34-118">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną wskazującą, czy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="6fd34-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="6fd34-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="6fd34-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6fd34-120">- RebootType</span><span class="sxs-lookup"><span data-stu-id="6fd34-120">-RebootType</span></span>
<span data-ttu-id="6fd34-121">Określa węzeł lub węzły do ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="6fd34-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="6fd34-122">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6fd34-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6fd34-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="6fd34-123">PrimaryNode</span></span> 
- <span data-ttu-id="6fd34-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="6fd34-124">SecondaryNode</span></span> 
- <span data-ttu-id="6fd34-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="6fd34-125">AllNodes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd34-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd34-126">-ResourceGroupName</span></span>
<span data-ttu-id="6fd34-127">Określa nazwę grupy zasobów, która zawiera pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="6fd34-127">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd34-128">-S s</span><span class="sxs-lookup"><span data-stu-id="6fd34-128">-ShardId</span></span>
<span data-ttu-id="6fd34-129">Określa identyfikator serwera, po ponownym uruchomieniu tego polecenia cmdlet dla pamięci podręcznej premium z włączonym grupowaniem.</span><span class="sxs-lookup"><span data-stu-id="6fd34-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd34-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6fd34-130">-Confirm</span></span>
<span data-ttu-id="6fd34-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6fd34-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd34-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd34-132">-WhatIf</span></span>
<span data-ttu-id="6fd34-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fd34-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fd34-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6fd34-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd34-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd34-135">CommonParameters</span></span>
<span data-ttu-id="6fd34-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd34-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd34-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd34-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd34-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fd34-138">INPUTS</span></span>

### <span data-ttu-id="6fd34-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6fd34-139">System.String</span></span>

### <span data-ttu-id="6fd34-140">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6fd34-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6fd34-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fd34-141">OUTPUTS</span></span>

### <span data-ttu-id="6fd34-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6fd34-142">System.Boolean</span></span>

## <span data-ttu-id="6fd34-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6fd34-143">NOTES</span></span>
* <span data-ttu-id="6fd34-144">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="6fd34-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="6fd34-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fd34-145">RELATED LINKS</span></span>

[<span data-ttu-id="6fd34-146">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd34-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="6fd34-147">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd34-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="6fd34-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd34-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="6fd34-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd34-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="6fd34-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd34-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


