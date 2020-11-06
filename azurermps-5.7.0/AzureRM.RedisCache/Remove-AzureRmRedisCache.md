---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: 4e49fbd2ac2604dab09d79255e7134fee02afd97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544180"
---
# <span data-ttu-id="3e68f-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e68f-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="3e68f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e68f-102">SYNOPSIS</span></span>
<span data-ttu-id="3e68f-103">Usuwa pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="3e68f-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e68f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e68f-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e68f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3e68f-105">DESCRIPTION</span></span>
<span data-ttu-id="3e68f-106">Polecenie cmdlet **Remove-AzureRmRedisCache** usuwa pamięć podręczną platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="3e68f-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="3e68f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e68f-107">EXAMPLES</span></span>

### <span data-ttu-id="3e68f-108">Przykład 1: Usunięcie pamięci podręcznej Redis i zwrócenie wyniku</span><span class="sxs-lookup"><span data-stu-id="3e68f-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="3e68f-109">To polecenie usuwa pamięć podręczną Redis i wyświetla, czy operacja jest udana.</span><span class="sxs-lookup"><span data-stu-id="3e68f-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="3e68f-110">Przykład 2: Usunięcie pamięci podręcznej Redis i nie Wyświetlanie wyniku</span><span class="sxs-lookup"><span data-stu-id="3e68f-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="3e68f-111">To polecenie usuwa pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="3e68f-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="3e68f-112">Ponieważ parametr *PassThru* nie jest określony, wynik operacji nie jest wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="3e68f-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="3e68f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e68f-113">PARAMETERS</span></span>

### <span data-ttu-id="3e68f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e68f-114">-DefaultProfile</span></span>
<span data-ttu-id="3e68f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e68f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e68f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3e68f-116">-Force</span></span>
<span data-ttu-id="3e68f-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3e68f-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e68f-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e68f-118">-Name</span></span>
<span data-ttu-id="3e68f-119">Określa nazwę pamięci podręcznej Redis do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="3e68f-119">Specifies the name of the Redis Cache to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e68f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e68f-120">-PassThru</span></span>
<span data-ttu-id="3e68f-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3e68f-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3e68f-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3e68f-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e68f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e68f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3e68f-124">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="3e68f-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e68f-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e68f-125">-Confirm</span></span>
<span data-ttu-id="3e68f-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e68f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e68f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e68f-127">-WhatIf</span></span>
<span data-ttu-id="3e68f-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e68f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e68f-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e68f-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e68f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e68f-130">CommonParameters</span></span>
<span data-ttu-id="3e68f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e68f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e68f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e68f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e68f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e68f-133">INPUTS</span></span>

### <span data-ttu-id="3e68f-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3e68f-134">None</span></span>
<span data-ttu-id="3e68f-135">Możesz popotokować dane wejściowe tego polecenia cmdlet za pomocą nazwy, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="3e68f-135">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="3e68f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e68f-136">OUTPUTS</span></span>

### <span data-ttu-id="3e68f-137">Wartość</span><span class="sxs-lookup"><span data-stu-id="3e68f-137">Boolean</span></span>
<span data-ttu-id="3e68f-138">Zwraca wartość $True, jeśli żaden wyjątek nie wystąpił.</span><span class="sxs-lookup"><span data-stu-id="3e68f-138">Returns $True if no exception occurs.</span></span>

## <span data-ttu-id="3e68f-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e68f-139">NOTES</span></span>

## <span data-ttu-id="3e68f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e68f-140">RELATED LINKS</span></span>

[<span data-ttu-id="3e68f-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e68f-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="3e68f-142">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e68f-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="3e68f-143">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e68f-143">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


