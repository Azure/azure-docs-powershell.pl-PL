---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: 12bf101fb404b02fc70cbec9640f5f2bd976107c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013521"
---
# <span data-ttu-id="43f11-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="43f11-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="43f11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43f11-102">SYNOPSIS</span></span>
<span data-ttu-id="43f11-103">Usuwa pamięć podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="43f11-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="43f11-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="43f11-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43f11-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="43f11-105">DESCRIPTION</span></span>
<span data-ttu-id="43f11-106">Polecenie **cmdlet Remove-AzHpcCache** usuwa pamięć podręczną Azure HPC Cache.</span><span class="sxs-lookup"><span data-stu-id="43f11-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="43f11-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="43f11-107">EXAMPLES</span></span>

### <span data-ttu-id="43f11-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="43f11-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="43f11-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43f11-109">PARAMETERS</span></span>

### <span data-ttu-id="43f11-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="43f11-110">-AsJob</span></span>
<span data-ttu-id="43f11-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="43f11-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43f11-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f11-112">-DefaultProfile</span></span>
<span data-ttu-id="43f11-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="43f11-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43f11-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="43f11-114">-Force</span></span>
<span data-ttu-id="43f11-115">Wskazuje, że polecenie cmdlet nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="43f11-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="43f11-116">Domyślnie to polecenie cmdlet wyświetla monit o potwierdzenie usunięcia pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="43f11-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="43f11-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="43f11-117">-Name</span></span>
<span data-ttu-id="43f11-118">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="43f11-118">Name of cache.</span></span>

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

### <span data-ttu-id="43f11-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43f11-119">-PassThru</span></span>
<span data-ttu-id="43f11-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="43f11-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="43f11-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="43f11-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="43f11-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43f11-122">-ResourceGroupName</span></span>
<span data-ttu-id="43f11-123">Nazwa grupy zasobów, w ramach której chcesz usunąć pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="43f11-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="43f11-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43f11-124">-Confirm</span></span>
<span data-ttu-id="43f11-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="43f11-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43f11-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f11-126">-WhatIf</span></span>
<span data-ttu-id="43f11-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43f11-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43f11-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="43f11-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43f11-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f11-129">CommonParameters</span></span>
<span data-ttu-id="43f11-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43f11-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f11-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43f11-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f11-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43f11-132">INPUTS</span></span>

### <span data-ttu-id="43f11-133">System.String</span><span class="sxs-lookup"><span data-stu-id="43f11-133">System.String</span></span>

## <span data-ttu-id="43f11-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43f11-134">OUTPUTS</span></span>

## <span data-ttu-id="43f11-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="43f11-135">NOTES</span></span>

## <span data-ttu-id="43f11-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43f11-136">RELATED LINKS</span></span>
