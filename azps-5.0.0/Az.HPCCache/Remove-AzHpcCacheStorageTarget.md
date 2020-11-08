---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232277"
---
# <span data-ttu-id="69313-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="69313-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="69313-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69313-102">SYNOPSIS</span></span>
<span data-ttu-id="69313-103">Usuwa miejsce docelowe miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="69313-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="69313-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69313-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69313-105">Opis</span><span class="sxs-lookup"><span data-stu-id="69313-105">DESCRIPTION</span></span>
<span data-ttu-id="69313-106">Polecenie cmdlet **Remove-AzHpcCacheStorageTarget** usuwa miejsce docelowe miejsca do magazynowania z pamięci podręcznej Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="69313-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="69313-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69313-107">EXAMPLES</span></span>

### <span data-ttu-id="69313-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69313-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="69313-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69313-109">PARAMETERS</span></span>

### <span data-ttu-id="69313-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69313-110">-AsJob</span></span>
<span data-ttu-id="69313-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="69313-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69313-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="69313-112">-CacheName</span></span>
<span data-ttu-id="69313-113">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="69313-113">Name of cache.</span></span>

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

### <span data-ttu-id="69313-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69313-114">-DefaultProfile</span></span>
<span data-ttu-id="69313-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69313-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69313-116">-Force</span><span class="sxs-lookup"><span data-stu-id="69313-116">-Force</span></span>
<span data-ttu-id="69313-117">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="69313-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="69313-118">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru usunięcia celu zapisu.</span><span class="sxs-lookup"><span data-stu-id="69313-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="69313-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="69313-119">-Name</span></span>
<span data-ttu-id="69313-120">Nazwa docelowego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="69313-120">Name of storage target.</span></span>

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

### <span data-ttu-id="69313-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69313-121">-PassThru</span></span>
<span data-ttu-id="69313-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="69313-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69313-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="69313-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="69313-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69313-124">-ResourceGroupName</span></span>
<span data-ttu-id="69313-125">Nazwa grupy zasobów, pod którą chcesz usunąć miejsce docelowe magazynu z pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="69313-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="69313-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69313-126">-Confirm</span></span>
<span data-ttu-id="69313-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69313-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69313-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69313-128">-WhatIf</span></span>
<span data-ttu-id="69313-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69313-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69313-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69313-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69313-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69313-131">CommonParameters</span></span>
<span data-ttu-id="69313-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69313-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69313-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69313-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69313-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69313-134">INPUTS</span></span>

### <span data-ttu-id="69313-135">System. String</span><span class="sxs-lookup"><span data-stu-id="69313-135">System.String</span></span>

## <span data-ttu-id="69313-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69313-136">OUTPUTS</span></span>

## <span data-ttu-id="69313-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69313-137">NOTES</span></span>

## <span data-ttu-id="69313-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69313-138">RELATED LINKS</span></span>
