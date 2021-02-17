---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243427"
---
# <span data-ttu-id="13b51-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="13b51-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="13b51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13b51-102">SYNOPSIS</span></span>
<span data-ttu-id="13b51-103">Aktualizuje tagi w pamięci podręcznej HPC.</span><span class="sxs-lookup"><span data-stu-id="13b51-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="13b51-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="13b51-104">SYNTAX</span></span>

### <span data-ttu-id="13b51-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="13b51-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13b51-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13b51-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13b51-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="13b51-107">DESCRIPTION</span></span>
<span data-ttu-id="13b51-108">Polecenie **cmdlet Set-AzHpcCache** aktualizuje tagi pamięci podręcznej Azure HPC Cache.</span><span class="sxs-lookup"><span data-stu-id="13b51-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="13b51-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="13b51-109">EXAMPLES</span></span>

### <span data-ttu-id="13b51-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13b51-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="13b51-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13b51-111">PARAMETERS</span></span>

### <span data-ttu-id="13b51-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="13b51-112">-AsJob</span></span>
<span data-ttu-id="13b51-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="13b51-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13b51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b51-114">-DefaultProfile</span></span>
<span data-ttu-id="13b51-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="13b51-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13b51-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13b51-116">-InputObject</span></span>
<span data-ttu-id="13b51-117">Obiekt pamięci podręcznej do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="13b51-117">The cache object to update.</span></span>

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

### <span data-ttu-id="13b51-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="13b51-118">-Name</span></span>
<span data-ttu-id="13b51-119">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="13b51-119">Name of cache.</span></span>

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

### <span data-ttu-id="13b51-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13b51-120">-ResourceGroupName</span></span>
<span data-ttu-id="13b51-121">Nazwa grupy zasobów, w ramach której chcesz zaktualizować pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="13b51-121">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="13b51-122">— Tag</span><span class="sxs-lookup"><span data-stu-id="13b51-122">-Tag</span></span>
<span data-ttu-id="13b51-123">Tagi, które należy skojarzyć z pamięcią podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="13b51-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b51-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13b51-124">-Confirm</span></span>
<span data-ttu-id="13b51-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="13b51-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13b51-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13b51-126">-WhatIf</span></span>
<span data-ttu-id="13b51-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13b51-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13b51-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="13b51-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13b51-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b51-129">CommonParameters</span></span>
<span data-ttu-id="13b51-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13b51-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b51-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13b51-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b51-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13b51-132">INPUTS</span></span>

### <span data-ttu-id="13b51-133">System.String</span><span class="sxs-lookup"><span data-stu-id="13b51-133">System.String</span></span>

### <span data-ttu-id="13b51-134">System.Int32</span><span class="sxs-lookup"><span data-stu-id="13b51-134">System.Int32</span></span>

## <span data-ttu-id="13b51-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13b51-135">OUTPUTS</span></span>

### <span data-ttu-id="13b51-136">Microsoft.Azure.PowerShell.Cmdlet.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="13b51-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="13b51-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="13b51-137">NOTES</span></span>

## <span data-ttu-id="13b51-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13b51-138">RELATED LINKS</span></span>
