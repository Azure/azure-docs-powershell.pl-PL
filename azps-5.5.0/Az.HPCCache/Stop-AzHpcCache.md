---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237740"
---
# <span data-ttu-id="e3fe9-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e3fe9-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="e3fe9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fe9-103">Zatrzymuje pamięć podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-103">Stops HPC cache.</span></span>

## <span data-ttu-id="e3fe9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e3fe9-104">SYNTAX</span></span>

### <span data-ttu-id="e3fe9-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e3fe9-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3fe9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3fe9-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3fe9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3fe9-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3fe9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e3fe9-108">DESCRIPTION</span></span>
<span data-ttu-id="e3fe9-109">Polecenie **cmdlet Stop-AzHpcCache** zatrzymuje pamięć podręczną Azure HPC Cache.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="e3fe9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e3fe9-110">EXAMPLES</span></span>

### <span data-ttu-id="e3fe9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e3fe9-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="e3fe9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3fe9-112">PARAMETERS</span></span>

### <span data-ttu-id="e3fe9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3fe9-113">-DefaultProfile</span></span>
<span data-ttu-id="e3fe9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3fe9-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e3fe9-115">-Force</span></span>
<span data-ttu-id="e3fe9-116">Wskazuje, że polecenie cmdlet nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="e3fe9-117">Domyślnie to polecenie cmdlet wyświetla monit o potwierdzenie, że chcesz zatrzymać pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="e3fe9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3fe9-118">-InputObject</span></span>
<span data-ttu-id="e3fe9-119">Obiekt pamięci podręcznej, który ma się zatrzymać.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-119">The cache object to stop.</span></span>

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

### <span data-ttu-id="e3fe9-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e3fe9-120">-Name</span></span>
<span data-ttu-id="e3fe9-121">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-121">Name of cache.</span></span>

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

### <span data-ttu-id="e3fe9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3fe9-122">-PassThru</span></span>
<span data-ttu-id="e3fe9-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e3fe9-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3fe9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3fe9-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3fe9-126">Nazwa grupy zasobów, w ramach której ma zostać zatrzymana pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-126">Name of resource group under which you want to stop cache.</span></span>

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

### <span data-ttu-id="e3fe9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3fe9-127">-ResourceId</span></span>
<span data-ttu-id="e3fe9-128">Identyfikator zasobu w pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="e3fe9-128">The resource id of the Cache</span></span>

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

### <span data-ttu-id="e3fe9-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3fe9-129">-Confirm</span></span>
<span data-ttu-id="e3fe9-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3fe9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3fe9-131">-WhatIf</span></span>
<span data-ttu-id="e3fe9-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3fe9-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3fe9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fe9-134">CommonParameters</span></span>
<span data-ttu-id="e3fe9-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3fe9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fe9-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3fe9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fe9-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3fe9-137">INPUTS</span></span>

### <span data-ttu-id="e3fe9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e3fe9-138">System.String</span></span>

## <span data-ttu-id="e3fe9-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e3fe9-139">OUTPUTS</span></span>

## <span data-ttu-id="e3fe9-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e3fe9-140">NOTES</span></span>

## <span data-ttu-id="e3fe9-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3fe9-141">RELATED LINKS</span></span>
