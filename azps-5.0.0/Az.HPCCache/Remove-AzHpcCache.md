---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232281"
---
# <span data-ttu-id="98ab8-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="98ab8-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="98ab8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="98ab8-103">Usuwa pamięć podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="98ab8-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="98ab8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98ab8-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98ab8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="98ab8-105">DESCRIPTION</span></span>
<span data-ttu-id="98ab8-106">Polecenie cmdlet **Remove-AzHpcCache** usuwa pamięć podręczną usługi Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="98ab8-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="98ab8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98ab8-107">EXAMPLES</span></span>

### <span data-ttu-id="98ab8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="98ab8-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="98ab8-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98ab8-109">PARAMETERS</span></span>

### <span data-ttu-id="98ab8-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98ab8-110">-AsJob</span></span>
<span data-ttu-id="98ab8-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="98ab8-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98ab8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ab8-112">-DefaultProfile</span></span>
<span data-ttu-id="98ab8-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98ab8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98ab8-114">-Force</span><span class="sxs-lookup"><span data-stu-id="98ab8-114">-Force</span></span>
<span data-ttu-id="98ab8-115">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="98ab8-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="98ab8-116">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru usunięcia pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="98ab8-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="98ab8-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98ab8-117">-Name</span></span>
<span data-ttu-id="98ab8-118">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="98ab8-118">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98ab8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98ab8-119">-PassThru</span></span>
<span data-ttu-id="98ab8-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="98ab8-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="98ab8-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="98ab8-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="98ab8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98ab8-122">-ResourceGroupName</span></span>
<span data-ttu-id="98ab8-123">Nazwa grupy zasobów, w której ma zostać usunięta pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="98ab8-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="98ab8-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98ab8-124">-Confirm</span></span>
<span data-ttu-id="98ab8-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98ab8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98ab8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98ab8-126">-WhatIf</span></span>
<span data-ttu-id="98ab8-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98ab8-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98ab8-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98ab8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98ab8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ab8-129">CommonParameters</span></span>
<span data-ttu-id="98ab8-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98ab8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ab8-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98ab8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ab8-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98ab8-132">INPUTS</span></span>

### <span data-ttu-id="98ab8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="98ab8-133">System.String</span></span>

## <span data-ttu-id="98ab8-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98ab8-134">OUTPUTS</span></span>

## <span data-ttu-id="98ab8-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98ab8-135">NOTES</span></span>

## <span data-ttu-id="98ab8-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98ab8-136">RELATED LINKS</span></span>
