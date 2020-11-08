---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222346"
---
# <span data-ttu-id="e489c-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e489c-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="e489c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e489c-102">SYNOPSIS</span></span>
<span data-ttu-id="e489c-103">Zatrzymuje pamięć podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="e489c-103">Stops HPC cache.</span></span>

## <span data-ttu-id="e489c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e489c-104">SYNTAX</span></span>

### <span data-ttu-id="e489c-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e489c-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e489c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e489c-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e489c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e489c-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e489c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e489c-108">DESCRIPTION</span></span>
<span data-ttu-id="e489c-109">Polecenie cmdlet **stop-AzHpcCache** zatrzymuje pamięć podręczną usługi Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="e489c-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="e489c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e489c-110">EXAMPLES</span></span>

### <span data-ttu-id="e489c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e489c-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="e489c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e489c-112">PARAMETERS</span></span>

### <span data-ttu-id="e489c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e489c-113">-DefaultProfile</span></span>
<span data-ttu-id="e489c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e489c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e489c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e489c-115">-Force</span></span>
<span data-ttu-id="e489c-116">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e489c-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="e489c-117">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru zatrzymania pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="e489c-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="e489c-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e489c-118">-InputObject</span></span>
<span data-ttu-id="e489c-119">Obiekt pamięci podręcznej, który ma zostać zatrzymany.</span><span class="sxs-lookup"><span data-stu-id="e489c-119">The cache object to stop.</span></span>

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

### <span data-ttu-id="e489c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e489c-120">-Name</span></span>
<span data-ttu-id="e489c-121">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="e489c-121">Name of cache.</span></span>

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

### <span data-ttu-id="e489c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e489c-122">-PassThru</span></span>
<span data-ttu-id="e489c-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e489c-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e489c-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e489c-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e489c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e489c-125">-ResourceGroupName</span></span>
<span data-ttu-id="e489c-126">Nazwa grupy zasobów, w której ma zostać zatrzymana pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="e489c-126">Name of resource group under which you want to stop cache.</span></span>

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

### <span data-ttu-id="e489c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e489c-127">-ResourceId</span></span>
<span data-ttu-id="e489c-128">Identyfikator zasobu w pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="e489c-128">The resource id of the Cache</span></span>

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

### <span data-ttu-id="e489c-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e489c-129">-Confirm</span></span>
<span data-ttu-id="e489c-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e489c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e489c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e489c-131">-WhatIf</span></span>
<span data-ttu-id="e489c-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e489c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e489c-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e489c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e489c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e489c-134">CommonParameters</span></span>
<span data-ttu-id="e489c-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e489c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e489c-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e489c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e489c-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e489c-137">INPUTS</span></span>

### <span data-ttu-id="e489c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e489c-138">System.String</span></span>

## <span data-ttu-id="e489c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e489c-139">OUTPUTS</span></span>

## <span data-ttu-id="e489c-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e489c-140">NOTES</span></span>

## <span data-ttu-id="e489c-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e489c-141">RELATED LINKS</span></span>
