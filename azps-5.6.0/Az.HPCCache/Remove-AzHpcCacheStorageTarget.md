---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: 2de3856a51ce8b55d6db7a82f6e50027b60d9d87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013514"
---
# <span data-ttu-id="fc642-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="fc642-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="fc642-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc642-102">SYNOPSIS</span></span>
<span data-ttu-id="fc642-103">Usuwa miejsce docelowe miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="fc642-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="fc642-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fc642-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc642-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fc642-105">DESCRIPTION</span></span>
<span data-ttu-id="fc642-106">Polecenie **cmdlet Remove-AzHpcCacheStorageTarget** usuwa element docelowy magazynu z pamięci podręcznej Azure HPC Cache.</span><span class="sxs-lookup"><span data-stu-id="fc642-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="fc642-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fc642-107">EXAMPLES</span></span>

### <span data-ttu-id="fc642-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fc642-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="fc642-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc642-109">PARAMETERS</span></span>

### <span data-ttu-id="fc642-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="fc642-110">-AsJob</span></span>
<span data-ttu-id="fc642-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fc642-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc642-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="fc642-112">-CacheName</span></span>
<span data-ttu-id="fc642-113">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="fc642-113">Name of cache.</span></span>

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

### <span data-ttu-id="fc642-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc642-114">-DefaultProfile</span></span>
<span data-ttu-id="fc642-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc642-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc642-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="fc642-116">-Force</span></span>
<span data-ttu-id="fc642-117">Wskazuje, że polecenie cmdlet nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fc642-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="fc642-118">Domyślnie to polecenie cmdlet wyświetla monit o potwierdzenie, że chcesz usunąć miejsce docelowe magazynu.</span><span class="sxs-lookup"><span data-stu-id="fc642-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="fc642-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fc642-119">-Name</span></span>
<span data-ttu-id="fc642-120">Nazwa miejsca docelowego magazynowania.</span><span class="sxs-lookup"><span data-stu-id="fc642-120">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc642-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc642-121">-PassThru</span></span>
<span data-ttu-id="fc642-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="fc642-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fc642-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fc642-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fc642-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc642-124">-ResourceGroupName</span></span>
<span data-ttu-id="fc642-125">Nazwa grupy zasobów, w ramach której chcesz usunąć element docelowy magazynu z pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="fc642-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="fc642-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc642-126">-Confirm</span></span>
<span data-ttu-id="fc642-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fc642-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc642-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc642-128">-WhatIf</span></span>
<span data-ttu-id="fc642-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc642-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc642-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fc642-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc642-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc642-131">CommonParameters</span></span>
<span data-ttu-id="fc642-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc642-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc642-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc642-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc642-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc642-134">INPUTS</span></span>

### <span data-ttu-id="fc642-135">System.String</span><span class="sxs-lookup"><span data-stu-id="fc642-135">System.String</span></span>

## <span data-ttu-id="fc642-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc642-136">OUTPUTS</span></span>

## <span data-ttu-id="fc642-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fc642-137">NOTES</span></span>

## <span data-ttu-id="fc642-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc642-138">RELATED LINKS</span></span>
