---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: 2e34bc9a468a662db8dc4bba155cd70a1c24bcfe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708492"
---
# <span data-ttu-id="8409d-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8409d-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="8409d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8409d-102">SYNOPSIS</span></span>
<span data-ttu-id="8409d-103">Ponownie uruchamia węzły pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="8409d-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="8409d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8409d-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8409d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8409d-105">DESCRIPTION</span></span>
<span data-ttu-id="8409d-106">Polecenie cmdlet **Reset-AzRedisCache** powoduje ponowne uruchomienie węzłów wystąpienia pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="8409d-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="8409d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8409d-107">EXAMPLES</span></span>

### <span data-ttu-id="8409d-108">Przykład 1. Uruchom ponownie oba węzły</span><span class="sxs-lookup"><span data-stu-id="8409d-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="8409d-109">To polecenie powoduje ponowne uruchomienie obu węzłów w pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="8409d-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="8409d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8409d-110">PARAMETERS</span></span>

### <span data-ttu-id="8409d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8409d-111">-DefaultProfile</span></span>
<span data-ttu-id="8409d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8409d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8409d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8409d-113">-Force</span></span>
<span data-ttu-id="8409d-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8409d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8409d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8409d-115">-Name</span></span>
<span data-ttu-id="8409d-116">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="8409d-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="8409d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8409d-117">-PassThru</span></span>
<span data-ttu-id="8409d-118">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną wskazującą, czy operacja kończy się pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="8409d-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="8409d-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8409d-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8409d-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="8409d-120">-RebootType</span></span>
<span data-ttu-id="8409d-121">Określa węzły, które mają zostać ponownie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8409d-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="8409d-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8409d-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8409d-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="8409d-123">PrimaryNode</span></span> 
- <span data-ttu-id="8409d-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="8409d-124">SecondaryNode</span></span> 
- <span data-ttu-id="8409d-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="8409d-125">AllNodes</span></span>

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

### <span data-ttu-id="8409d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8409d-126">-ResourceGroupName</span></span>
<span data-ttu-id="8409d-127">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="8409d-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="8409d-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="8409d-128">-ShardId</span></span>
<span data-ttu-id="8409d-129">Określa identyfikator Shard, który zostanie ponownie uruchomiony przez to polecenie cmdlet dla Premium pamięci podręcznej z włączoną funkcją klastrowania.</span><span class="sxs-lookup"><span data-stu-id="8409d-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="8409d-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8409d-130">-Confirm</span></span>
<span data-ttu-id="8409d-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8409d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8409d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8409d-132">-WhatIf</span></span>
<span data-ttu-id="8409d-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8409d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8409d-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8409d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8409d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8409d-135">CommonParameters</span></span>
<span data-ttu-id="8409d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8409d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8409d-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8409d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8409d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8409d-138">INPUTS</span></span>

### <span data-ttu-id="8409d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8409d-139">System.String</span></span>

### <span data-ttu-id="8409d-140">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8409d-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8409d-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8409d-141">OUTPUTS</span></span>

### <span data-ttu-id="8409d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8409d-142">System.Boolean</span></span>

## <span data-ttu-id="8409d-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8409d-143">NOTES</span></span>
* <span data-ttu-id="8409d-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="8409d-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="8409d-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8409d-145">RELATED LINKS</span></span>

[<span data-ttu-id="8409d-146">Eksportowanie — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8409d-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="8409d-147">Import — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8409d-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="8409d-148">Nowe — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8409d-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="8409d-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8409d-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="8409d-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8409d-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


