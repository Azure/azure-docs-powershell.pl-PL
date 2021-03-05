---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 2ae4c2d5de8eeba370c981ceb5a94baa1ba91cf2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960129"
---
# <span data-ttu-id="d1930-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d1930-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="d1930-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1930-102">SYNOPSIS</span></span>
<span data-ttu-id="d1930-103">Usuwa pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="d1930-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="d1930-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d1930-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1930-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d1930-105">DESCRIPTION</span></span>
<span data-ttu-id="d1930-106">Polecenie **cmdlet Remove-AzRedisCache** usuwa pamięć podręczną Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="d1930-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="d1930-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d1930-107">EXAMPLES</span></span>

### <span data-ttu-id="d1930-108">Przykład 1. Usunięcie pamięci podręcznej Redis i zwrócenie wyniku</span><span class="sxs-lookup"><span data-stu-id="d1930-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="d1930-109">To polecenie usuwa pamięć podręczną Redis i wyświetla, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="d1930-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="d1930-110">Przykład 2. Usunięcie pamięci podręcznej Redis i nie wyświetlanie wyniku</span><span class="sxs-lookup"><span data-stu-id="d1930-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="d1930-111">To polecenie usuwa pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="d1930-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="d1930-112">Parametr *PassThru* nie jest określony, dlatego wynik operacji nie jest wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="d1930-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="d1930-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1930-113">PARAMETERS</span></span>

### <span data-ttu-id="d1930-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1930-114">-DefaultProfile</span></span>
<span data-ttu-id="d1930-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1930-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1930-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d1930-116">-Force</span></span>
<span data-ttu-id="d1930-117">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d1930-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d1930-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d1930-118">-Name</span></span>
<span data-ttu-id="d1930-119">Określa nazwę pamięci podręcznej Redis, która ma być usuwana.</span><span class="sxs-lookup"><span data-stu-id="d1930-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="d1930-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1930-120">-PassThru</span></span>
<span data-ttu-id="d1930-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d1930-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d1930-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d1930-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d1930-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1930-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1930-124">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d1930-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="d1930-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1930-125">-Confirm</span></span>
<span data-ttu-id="d1930-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d1930-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1930-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1930-127">-WhatIf</span></span>
<span data-ttu-id="d1930-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1930-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1930-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d1930-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1930-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1930-130">CommonParameters</span></span>
<span data-ttu-id="d1930-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1930-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1930-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1930-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1930-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1930-133">INPUTS</span></span>

### <span data-ttu-id="d1930-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d1930-134">System.String</span></span>

## <span data-ttu-id="d1930-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1930-135">OUTPUTS</span></span>

### <span data-ttu-id="d1930-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d1930-136">System.Boolean</span></span>

## <span data-ttu-id="d1930-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d1930-137">NOTES</span></span>

## <span data-ttu-id="d1930-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1930-138">RELATED LINKS</span></span>

[<span data-ttu-id="d1930-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d1930-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="d1930-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d1930-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="d1930-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d1930-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


