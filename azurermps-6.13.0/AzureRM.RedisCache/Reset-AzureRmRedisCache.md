---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/reset-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: 8aad14bde950a5e98d8d9331428a62e957cb0afe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552579"
---
# <span data-ttu-id="e9192-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e9192-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="e9192-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9192-102">SYNOPSIS</span></span>
<span data-ttu-id="e9192-103">Ponownie uruchamia węzły pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="e9192-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9192-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9192-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9192-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e9192-105">DESCRIPTION</span></span>
<span data-ttu-id="e9192-106">Polecenie cmdlet **Reset-AzureRmRedisCache** powoduje ponowne uruchomienie węzłów wystąpienia pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="e9192-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="e9192-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9192-107">EXAMPLES</span></span>

### <span data-ttu-id="e9192-108">Przykład 1. Uruchom ponownie oba węzły</span><span class="sxs-lookup"><span data-stu-id="e9192-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="e9192-109">To polecenie powoduje ponowne uruchomienie obu węzłów w pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="e9192-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="e9192-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9192-110">PARAMETERS</span></span>

### <span data-ttu-id="e9192-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9192-111">-DefaultProfile</span></span>
<span data-ttu-id="e9192-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9192-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9192-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e9192-113">-Force</span></span>
<span data-ttu-id="e9192-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e9192-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e9192-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e9192-115">-Name</span></span>
<span data-ttu-id="e9192-116">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="e9192-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="e9192-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9192-117">-PassThru</span></span>
<span data-ttu-id="e9192-118">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną wskazującą, czy operacja kończy się pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="e9192-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="e9192-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e9192-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e9192-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="e9192-120">-RebootType</span></span>
<span data-ttu-id="e9192-121">Określa węzły, które mają zostać ponownie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e9192-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="e9192-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e9192-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e9192-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="e9192-123">PrimaryNode</span></span> 
- <span data-ttu-id="e9192-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="e9192-124">SecondaryNode</span></span> 
- <span data-ttu-id="e9192-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="e9192-125">AllNodes</span></span>

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

### <span data-ttu-id="e9192-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9192-126">-ResourceGroupName</span></span>
<span data-ttu-id="e9192-127">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="e9192-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="e9192-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="e9192-128">-ShardId</span></span>
<span data-ttu-id="e9192-129">Określa identyfikator Shard, który zostanie ponownie uruchomiony przez to polecenie cmdlet dla Premium pamięci podręcznej z włączoną funkcją klastrowania.</span><span class="sxs-lookup"><span data-stu-id="e9192-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="e9192-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9192-130">-Confirm</span></span>
<span data-ttu-id="e9192-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9192-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9192-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9192-132">-WhatIf</span></span>
<span data-ttu-id="e9192-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9192-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9192-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e9192-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9192-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9192-135">CommonParameters</span></span>
<span data-ttu-id="e9192-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9192-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9192-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9192-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9192-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9192-138">INPUTS</span></span>

### <span data-ttu-id="e9192-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e9192-139">System.String</span></span>

### <span data-ttu-id="e9192-140">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e9192-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e9192-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9192-141">OUTPUTS</span></span>

### <span data-ttu-id="e9192-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9192-142">System.Boolean</span></span>

## <span data-ttu-id="e9192-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9192-143">NOTES</span></span>
* <span data-ttu-id="e9192-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="e9192-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="e9192-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9192-145">RELATED LINKS</span></span>

[<span data-ttu-id="e9192-146">Eksportowanie — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e9192-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="e9192-147">Import — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e9192-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="e9192-148">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e9192-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="e9192-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e9192-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="e9192-150">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e9192-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

