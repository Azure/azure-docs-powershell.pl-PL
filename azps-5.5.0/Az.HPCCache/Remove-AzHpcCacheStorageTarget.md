---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243434"
---
# <span data-ttu-id="74d0f-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="74d0f-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="74d0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="74d0f-103">Usuwa miejsce docelowe miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="74d0f-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="74d0f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74d0f-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74d0f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="74d0f-105">DESCRIPTION</span></span>
<span data-ttu-id="74d0f-106">Polecenie **cmdlet Remove-AzHpcCacheStorageTarget** usuwa element docelowy magazynu z pamięci podręcznej Azure HPC Cache.</span><span class="sxs-lookup"><span data-stu-id="74d0f-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="74d0f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74d0f-107">EXAMPLES</span></span>

### <span data-ttu-id="74d0f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="74d0f-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="74d0f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74d0f-109">PARAMETERS</span></span>

### <span data-ttu-id="74d0f-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="74d0f-110">-AsJob</span></span>
<span data-ttu-id="74d0f-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="74d0f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74d0f-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="74d0f-112">-CacheName</span></span>
<span data-ttu-id="74d0f-113">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="74d0f-113">Name of cache.</span></span>

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

### <span data-ttu-id="74d0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d0f-114">-DefaultProfile</span></span>
<span data-ttu-id="74d0f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74d0f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74d0f-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="74d0f-116">-Force</span></span>
<span data-ttu-id="74d0f-117">Wskazuje, że polecenie cmdlet nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74d0f-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="74d0f-118">Domyślnie to polecenie cmdlet wyświetla monit o potwierdzenie, że chcesz usunąć miejsce docelowe magazynu.</span><span class="sxs-lookup"><span data-stu-id="74d0f-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="74d0f-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="74d0f-119">-Name</span></span>
<span data-ttu-id="74d0f-120">Nazwa miejsca docelowego magazynowania.</span><span class="sxs-lookup"><span data-stu-id="74d0f-120">Name of storage target.</span></span>

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

### <span data-ttu-id="74d0f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74d0f-121">-PassThru</span></span>
<span data-ttu-id="74d0f-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="74d0f-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="74d0f-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="74d0f-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="74d0f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74d0f-124">-ResourceGroupName</span></span>
<span data-ttu-id="74d0f-125">Nazwa grupy zasobów, w ramach której chcesz usunąć element docelowy magazynu z pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="74d0f-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="74d0f-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74d0f-126">-Confirm</span></span>
<span data-ttu-id="74d0f-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74d0f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d0f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d0f-128">-WhatIf</span></span>
<span data-ttu-id="74d0f-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74d0f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74d0f-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="74d0f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d0f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d0f-131">CommonParameters</span></span>
<span data-ttu-id="74d0f-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d0f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d0f-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74d0f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d0f-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74d0f-134">INPUTS</span></span>

### <span data-ttu-id="74d0f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="74d0f-135">System.String</span></span>

## <span data-ttu-id="74d0f-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74d0f-136">OUTPUTS</span></span>

## <span data-ttu-id="74d0f-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74d0f-137">NOTES</span></span>

## <span data-ttu-id="74d0f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74d0f-138">RELATED LINKS</span></span>
