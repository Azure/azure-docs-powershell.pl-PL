---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: 35b7d3e05cced593da748f430cb121da43cd0380
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550252"
---
# <span data-ttu-id="b09cf-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b09cf-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="b09cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b09cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b09cf-103">Usuwa pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="b09cf-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b09cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b09cf-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b09cf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b09cf-105">DESCRIPTION</span></span>
<span data-ttu-id="b09cf-106">Polecenie cmdlet **Remove-AzureRmRedisCache** usuwa pamięć podręczną platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="b09cf-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="b09cf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b09cf-107">EXAMPLES</span></span>

### <span data-ttu-id="b09cf-108">Przykład 1: Usunięcie pamięci podręcznej Redis i zwrócenie wyniku</span><span class="sxs-lookup"><span data-stu-id="b09cf-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="b09cf-109">To polecenie usuwa pamięć podręczną Redis i wyświetla, czy operacja jest udana.</span><span class="sxs-lookup"><span data-stu-id="b09cf-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="b09cf-110">Przykład 2: Usunięcie pamięci podręcznej Redis i nie Wyświetlanie wyniku</span><span class="sxs-lookup"><span data-stu-id="b09cf-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="b09cf-111">To polecenie usuwa pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="b09cf-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="b09cf-112">Ponieważ parametr *PassThru* nie jest określony, wynik operacji nie jest wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="b09cf-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="b09cf-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b09cf-113">PARAMETERS</span></span>

### <span data-ttu-id="b09cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b09cf-114">-DefaultProfile</span></span>
<span data-ttu-id="b09cf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b09cf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b09cf-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b09cf-116">-Force</span></span>
<span data-ttu-id="b09cf-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b09cf-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b09cf-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b09cf-118">-Name</span></span>
<span data-ttu-id="b09cf-119">Określa nazwę pamięci podręcznej Redis do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b09cf-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="b09cf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b09cf-120">-PassThru</span></span>
<span data-ttu-id="b09cf-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b09cf-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b09cf-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b09cf-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b09cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b09cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="b09cf-124">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b09cf-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="b09cf-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b09cf-125">-Confirm</span></span>
<span data-ttu-id="b09cf-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b09cf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b09cf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b09cf-127">-WhatIf</span></span>
<span data-ttu-id="b09cf-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b09cf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b09cf-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b09cf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b09cf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b09cf-130">CommonParameters</span></span>
<span data-ttu-id="b09cf-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b09cf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b09cf-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b09cf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b09cf-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b09cf-133">INPUTS</span></span>

### <span data-ttu-id="b09cf-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b09cf-134">System.String</span></span>

## <span data-ttu-id="b09cf-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b09cf-135">OUTPUTS</span></span>

### <span data-ttu-id="b09cf-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b09cf-136">System.Boolean</span></span>

## <span data-ttu-id="b09cf-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b09cf-137">NOTES</span></span>

## <span data-ttu-id="b09cf-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b09cf-138">RELATED LINKS</span></span>

[<span data-ttu-id="b09cf-139">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b09cf-139">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="b09cf-140">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b09cf-140">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="b09cf-141">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b09cf-141">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

