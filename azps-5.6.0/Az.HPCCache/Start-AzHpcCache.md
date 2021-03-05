---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 29ab4c0536b64203af540f08d0a1974371812c19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013482"
---
# <span data-ttu-id="d5c25-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="d5c25-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="d5c25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5c25-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c25-103">Uruchamia pamięć podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="d5c25-103">Starts HPC cache.</span></span>

## <span data-ttu-id="d5c25-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d5c25-104">SYNTAX</span></span>

### <span data-ttu-id="d5c25-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d5c25-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c25-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5c25-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c25-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5c25-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5c25-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d5c25-108">DESCRIPTION</span></span>
<span data-ttu-id="d5c25-109">Polecenie **cmdlet Start-AzHpcCache** uruchamia pamięć podręczną Azure HPC Cache.</span><span class="sxs-lookup"><span data-stu-id="d5c25-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="d5c25-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d5c25-110">EXAMPLES</span></span>

### <span data-ttu-id="d5c25-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d5c25-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="d5c25-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5c25-112">PARAMETERS</span></span>

### <span data-ttu-id="d5c25-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d5c25-113">-AsJob</span></span>
<span data-ttu-id="d5c25-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d5c25-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5c25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c25-115">-DefaultProfile</span></span>
<span data-ttu-id="d5c25-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5c25-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5c25-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d5c25-117">-Force</span></span>
<span data-ttu-id="d5c25-118">Wskazuje, że polecenie cmdlet nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d5c25-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="d5c25-119">Domyślnie to polecenie cmdlet wyświetla monit o potwierdzenie, że chcesz uruchomić pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="d5c25-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="d5c25-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5c25-120">-InputObject</span></span>
<span data-ttu-id="d5c25-121">Obiekt pamięci podręcznej, który ma się rozpocząć.</span><span class="sxs-lookup"><span data-stu-id="d5c25-121">The cache object to start.</span></span>

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

### <span data-ttu-id="d5c25-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d5c25-122">-Name</span></span>
<span data-ttu-id="d5c25-123">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="d5c25-123">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c25-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5c25-124">-PassThru</span></span>
<span data-ttu-id="d5c25-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d5c25-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d5c25-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d5c25-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d5c25-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5c25-127">-ResourceGroupName</span></span>
<span data-ttu-id="d5c25-128">Nazwa grupy zasobów, w której chcesz uruchomić pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="d5c25-128">Name of resource group under which you want to start cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c25-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5c25-129">-ResourceId</span></span>
<span data-ttu-id="d5c25-130">Identyfikator zasobu pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="d5c25-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="d5c25-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d5c25-131">-Confirm</span></span>
<span data-ttu-id="d5c25-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d5c25-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5c25-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5c25-133">-WhatIf</span></span>
<span data-ttu-id="d5c25-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5c25-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5c25-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d5c25-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5c25-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c25-136">CommonParameters</span></span>
<span data-ttu-id="d5c25-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c25-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c25-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5c25-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c25-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5c25-139">INPUTS</span></span>

### <span data-ttu-id="d5c25-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d5c25-140">System.String</span></span>

## <span data-ttu-id="d5c25-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5c25-141">OUTPUTS</span></span>

## <span data-ttu-id="d5c25-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d5c25-142">NOTES</span></span>

## <span data-ttu-id="d5c25-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5c25-143">RELATED LINKS</span></span>
