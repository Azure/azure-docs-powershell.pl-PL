---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 1e9895b78bc61155f7cabfc63e6fb5e4cfbcd30d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708505"
---
# <span data-ttu-id="76aec-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="76aec-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="76aec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76aec-102">SYNOPSIS</span></span>
<span data-ttu-id="76aec-103">Usuwa pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="76aec-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="76aec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76aec-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76aec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="76aec-105">DESCRIPTION</span></span>
<span data-ttu-id="76aec-106">Polecenie cmdlet **Remove-AzRedisCache** usuwa pamięć podręczną platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="76aec-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="76aec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76aec-107">EXAMPLES</span></span>

### <span data-ttu-id="76aec-108">Przykład 1: Usunięcie pamięci podręcznej Redis i zwrócenie wyniku</span><span class="sxs-lookup"><span data-stu-id="76aec-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="76aec-109">To polecenie usuwa pamięć podręczną Redis i wyświetla, czy operacja jest udana.</span><span class="sxs-lookup"><span data-stu-id="76aec-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="76aec-110">Przykład 2: Usunięcie pamięci podręcznej Redis i nie Wyświetlanie wyniku</span><span class="sxs-lookup"><span data-stu-id="76aec-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="76aec-111">To polecenie usuwa pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="76aec-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="76aec-112">Ponieważ parametr *PassThru* nie jest określony, wynik operacji nie jest wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="76aec-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="76aec-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76aec-113">PARAMETERS</span></span>

### <span data-ttu-id="76aec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76aec-114">-DefaultProfile</span></span>
<span data-ttu-id="76aec-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76aec-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76aec-116">-Force</span><span class="sxs-lookup"><span data-stu-id="76aec-116">-Force</span></span>
<span data-ttu-id="76aec-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="76aec-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="76aec-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76aec-118">-Name</span></span>
<span data-ttu-id="76aec-119">Określa nazwę pamięci podręcznej Redis do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="76aec-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="76aec-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76aec-120">-PassThru</span></span>
<span data-ttu-id="76aec-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="76aec-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="76aec-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="76aec-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="76aec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76aec-123">-ResourceGroupName</span></span>
<span data-ttu-id="76aec-124">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="76aec-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="76aec-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76aec-125">-Confirm</span></span>
<span data-ttu-id="76aec-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76aec-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76aec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76aec-127">-WhatIf</span></span>
<span data-ttu-id="76aec-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76aec-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76aec-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="76aec-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76aec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76aec-130">CommonParameters</span></span>
<span data-ttu-id="76aec-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76aec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76aec-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76aec-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76aec-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76aec-133">INPUTS</span></span>

### <span data-ttu-id="76aec-134">System. String</span><span class="sxs-lookup"><span data-stu-id="76aec-134">System.String</span></span>

## <span data-ttu-id="76aec-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76aec-135">OUTPUTS</span></span>

### <span data-ttu-id="76aec-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76aec-136">System.Boolean</span></span>

## <span data-ttu-id="76aec-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76aec-137">NOTES</span></span>

## <span data-ttu-id="76aec-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76aec-138">RELATED LINKS</span></span>

[<span data-ttu-id="76aec-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="76aec-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="76aec-140">Nowe — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="76aec-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="76aec-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="76aec-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)

