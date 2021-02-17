---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: f48d49a59b21cbae3f314926f4de92e74a2b10e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240227"
---
# <span data-ttu-id="2fac2-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="2fac2-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="2fac2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fac2-102">SYNOPSIS</span></span>
<span data-ttu-id="2fac2-103">Ponownie generuje klucz dostępu pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="2fac2-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="2fac2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2fac2-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fac2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2fac2-105">DESCRIPTION</span></span>
<span data-ttu-id="2fac2-106">Polecenie **cmdlet New-AzRedisCacheKey** ponownie generuje klucz dostępu w usłudze Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="2fac2-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="2fac2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2fac2-107">EXAMPLES</span></span>

### <span data-ttu-id="2fac2-108">Przykład 1. Ponowne generowanie klucza podstawowego</span><span class="sxs-lookup"><span data-stu-id="2fac2-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="2fac2-109">To polecenie ponownie generuje klucz podstawowy pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="2fac2-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="2fac2-110">Przykład 2. Ponowne generowanie klucza pomocniczego</span><span class="sxs-lookup"><span data-stu-id="2fac2-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="2fac2-111">To polecenie ponownie generuje klucz pomocniczy pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="2fac2-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="2fac2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fac2-112">PARAMETERS</span></span>

### <span data-ttu-id="2fac2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fac2-113">-DefaultProfile</span></span>
<span data-ttu-id="2fac2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fac2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fac2-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2fac2-115">-Force</span></span>
<span data-ttu-id="2fac2-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2fac2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2fac2-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="2fac2-117">-KeyType</span></span>
<span data-ttu-id="2fac2-118">Określa, czy ponownie wygenerować klucz dostępu podstawowy, czy pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="2fac2-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="2fac2-119">Prawidłowe wartości to: Podstawowy, Pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="2fac2-119">Valid values are: Primary, Secondary.</span></span>

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

### <span data-ttu-id="2fac2-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2fac2-120">-Name</span></span>
<span data-ttu-id="2fac2-121">Określa nazwę pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="2fac2-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="2fac2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fac2-122">-ResourceGroupName</span></span>
<span data-ttu-id="2fac2-123">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="2fac2-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="2fac2-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2fac2-124">-Confirm</span></span>
<span data-ttu-id="2fac2-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2fac2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fac2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fac2-126">-WhatIf</span></span>
<span data-ttu-id="2fac2-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fac2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fac2-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2fac2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fac2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fac2-129">CommonParameters</span></span>
<span data-ttu-id="2fac2-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fac2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fac2-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fac2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fac2-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fac2-132">INPUTS</span></span>

### <span data-ttu-id="2fac2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2fac2-133">System.String</span></span>

## <span data-ttu-id="2fac2-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2fac2-134">OUTPUTS</span></span>

### <span data-ttu-id="2fac2-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="2fac2-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="2fac2-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2fac2-136">NOTES</span></span>

## <span data-ttu-id="2fac2-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fac2-137">RELATED LINKS</span></span>

[<span data-ttu-id="2fac2-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="2fac2-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)


