---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: fb9a46037aa550ee252546a5c7f4345299d4ffba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708511"
---
# <span data-ttu-id="03c57-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="03c57-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="03c57-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03c57-102">SYNOPSIS</span></span>
<span data-ttu-id="03c57-103">Generuje ponownie klucz dostępu pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="03c57-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="03c57-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03c57-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c57-105">Opis</span><span class="sxs-lookup"><span data-stu-id="03c57-105">DESCRIPTION</span></span>
<span data-ttu-id="03c57-106">Polecenie cmdlet **New-AzRedisCacheKey** generuje klucz dostępu do pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="03c57-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="03c57-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03c57-107">EXAMPLES</span></span>

### <span data-ttu-id="03c57-108">Przykład 1. Regeneruj klucz podstawowy</span><span class="sxs-lookup"><span data-stu-id="03c57-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="03c57-109">To polecenie generuje ponownie klucz podstawowy pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="03c57-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="03c57-110">Przykład 2: ponowne wygenerowanie klucza pomocniczego</span><span class="sxs-lookup"><span data-stu-id="03c57-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="03c57-111">To polecenie generuje ponownie klucz pomocniczy pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="03c57-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="03c57-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03c57-112">PARAMETERS</span></span>

### <span data-ttu-id="03c57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c57-113">-DefaultProfile</span></span>
<span data-ttu-id="03c57-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03c57-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03c57-115">-Force</span><span class="sxs-lookup"><span data-stu-id="03c57-115">-Force</span></span>
<span data-ttu-id="03c57-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="03c57-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03c57-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="03c57-117">-KeyType</span></span>
<span data-ttu-id="03c57-118">Określa, czy ponownie wygenerować podstawowy lub pomocniczy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="03c57-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="03c57-119">Prawidłowe wartości: podstawowy, pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="03c57-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c57-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03c57-120">-Name</span></span>
<span data-ttu-id="03c57-121">Określa nazwę pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="03c57-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="03c57-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c57-122">-ResourceGroupName</span></span>
<span data-ttu-id="03c57-123">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="03c57-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="03c57-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03c57-124">-Confirm</span></span>
<span data-ttu-id="03c57-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03c57-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c57-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c57-126">-WhatIf</span></span>
<span data-ttu-id="03c57-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03c57-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c57-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03c57-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c57-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c57-129">CommonParameters</span></span>
<span data-ttu-id="03c57-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c57-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c57-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03c57-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c57-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03c57-132">INPUTS</span></span>

### <span data-ttu-id="03c57-133">System. String</span><span class="sxs-lookup"><span data-stu-id="03c57-133">System.String</span></span>

## <span data-ttu-id="03c57-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03c57-134">OUTPUTS</span></span>

### <span data-ttu-id="03c57-135">Microsoft. Azure. Management. Redis. MODELES. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="03c57-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="03c57-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03c57-136">NOTES</span></span>

## <span data-ttu-id="03c57-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03c57-137">RELATED LINKS</span></span>

[<span data-ttu-id="03c57-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="03c57-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)


