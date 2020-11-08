---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224314"
---
# <span data-ttu-id="51609-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="51609-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="51609-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51609-102">SYNOPSIS</span></span>
<span data-ttu-id="51609-103">Aktualizuje pamięć podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="51609-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="51609-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51609-104">SYNTAX</span></span>

### <span data-ttu-id="51609-105">FlushParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="51609-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51609-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51609-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51609-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="51609-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51609-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51609-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51609-109">Opis</span><span class="sxs-lookup"><span data-stu-id="51609-109">DESCRIPTION</span></span>
<span data-ttu-id="51609-110">Polecenie cmdlet **Update-AzHpcCache** aktualizuje pamięć podręczną usługi Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="51609-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="51609-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51609-111">EXAMPLES</span></span>

### <span data-ttu-id="51609-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51609-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="51609-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51609-113">PARAMETERS</span></span>

### <span data-ttu-id="51609-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51609-114">-AsJob</span></span>
<span data-ttu-id="51609-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="51609-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51609-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51609-116">-DefaultProfile</span></span>
<span data-ttu-id="51609-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51609-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51609-118">-Flush</span><span class="sxs-lookup"><span data-stu-id="51609-118">-Flush</span></span>
<span data-ttu-id="51609-119">Opróżnia bufor HPC.</span><span class="sxs-lookup"><span data-stu-id="51609-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51609-120">-Force</span><span class="sxs-lookup"><span data-stu-id="51609-120">-Force</span></span>
<span data-ttu-id="51609-121">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="51609-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="51609-122">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru zaktualizowania pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="51609-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="51609-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="51609-123">-InputObject</span></span>
<span data-ttu-id="51609-124">Obiekt pamięci podręcznej do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="51609-124">The cache object to update.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51609-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51609-125">-Name</span></span>
<span data-ttu-id="51609-126">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="51609-126">Name of cache.</span></span>

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

### <span data-ttu-id="51609-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51609-127">-PassThru</span></span>
<span data-ttu-id="51609-128">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="51609-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="51609-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="51609-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="51609-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51609-130">-ResourceGroupName</span></span>
<span data-ttu-id="51609-131">Nazwa grupy zasobów, pod którą ma zostać zaktualizowana pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="51609-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="51609-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51609-132">-ResourceId</span></span>
<span data-ttu-id="51609-133">Identyfikator zasobu w pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="51609-133">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51609-134">— Uaktualnienie</span><span class="sxs-lookup"><span data-stu-id="51609-134">-Upgrade</span></span>
<span data-ttu-id="51609-135">Uaktualnij HpcCache.</span><span class="sxs-lookup"><span data-stu-id="51609-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51609-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51609-136">-Confirm</span></span>
<span data-ttu-id="51609-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51609-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51609-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51609-138">-WhatIf</span></span>
<span data-ttu-id="51609-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51609-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51609-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="51609-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51609-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51609-141">CommonParameters</span></span>
<span data-ttu-id="51609-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51609-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51609-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51609-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51609-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51609-144">INPUTS</span></span>

### <span data-ttu-id="51609-145">System. String</span><span class="sxs-lookup"><span data-stu-id="51609-145">System.String</span></span>

## <span data-ttu-id="51609-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51609-146">OUTPUTS</span></span>

## <span data-ttu-id="51609-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51609-147">NOTES</span></span>

## <span data-ttu-id="51609-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51609-148">RELATED LINKS</span></span>
