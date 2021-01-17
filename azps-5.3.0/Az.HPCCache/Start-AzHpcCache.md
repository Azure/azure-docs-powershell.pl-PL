---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489558"
---
# <span data-ttu-id="f2502-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="f2502-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="f2502-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2502-102">SYNOPSIS</span></span>
<span data-ttu-id="f2502-103">Uruchamia pamięć podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="f2502-103">Starts HPC cache.</span></span>

## <span data-ttu-id="f2502-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2502-104">SYNTAX</span></span>

### <span data-ttu-id="f2502-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f2502-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2502-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2502-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2502-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2502-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2502-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f2502-108">DESCRIPTION</span></span>
<span data-ttu-id="f2502-109">Polecenie cmdlet **Start-AzHpcCache** uruchamia pamięć podręczną usługi Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="f2502-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="f2502-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2502-110">EXAMPLES</span></span>

### <span data-ttu-id="f2502-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2502-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="f2502-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2502-112">PARAMETERS</span></span>

### <span data-ttu-id="f2502-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2502-113">-AsJob</span></span>
<span data-ttu-id="f2502-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f2502-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2502-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2502-115">-DefaultProfile</span></span>
<span data-ttu-id="f2502-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2502-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2502-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f2502-117">-Force</span></span>
<span data-ttu-id="f2502-118">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f2502-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="f2502-119">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru uruchomienia pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="f2502-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="f2502-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f2502-120">-InputObject</span></span>
<span data-ttu-id="f2502-121">Obiekt pamięci podręcznej, który ma zostać uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="f2502-121">The cache object to start.</span></span>

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

### <span data-ttu-id="f2502-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f2502-122">-Name</span></span>
<span data-ttu-id="f2502-123">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="f2502-123">Name of cache.</span></span>

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

### <span data-ttu-id="f2502-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2502-124">-PassThru</span></span>
<span data-ttu-id="f2502-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f2502-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f2502-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f2502-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f2502-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2502-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2502-128">Nazwa grupy zasobów, w której ma zostać rozpoczęta pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="f2502-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="f2502-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2502-129">-ResourceId</span></span>
<span data-ttu-id="f2502-130">Identyfikator zasobu w pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="f2502-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="f2502-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2502-131">-Confirm</span></span>
<span data-ttu-id="f2502-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2502-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2502-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2502-133">-WhatIf</span></span>
<span data-ttu-id="f2502-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2502-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2502-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f2502-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2502-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2502-136">CommonParameters</span></span>
<span data-ttu-id="f2502-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2502-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2502-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2502-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2502-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2502-139">INPUTS</span></span>

### <span data-ttu-id="f2502-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f2502-140">System.String</span></span>

## <span data-ttu-id="f2502-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2502-141">OUTPUTS</span></span>

## <span data-ttu-id="f2502-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2502-142">NOTES</span></span>

## <span data-ttu-id="f2502-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2502-143">RELATED LINKS</span></span>
