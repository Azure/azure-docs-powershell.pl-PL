---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231861"
---
# <span data-ttu-id="873db-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="873db-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="873db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="873db-102">SYNOPSIS</span></span>
<span data-ttu-id="873db-103">Uruchamia pamięć podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="873db-103">Starts HPC cache.</span></span>

## <span data-ttu-id="873db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="873db-104">SYNTAX</span></span>

### <span data-ttu-id="873db-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="873db-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="873db-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="873db-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="873db-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="873db-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="873db-108">Opis</span><span class="sxs-lookup"><span data-stu-id="873db-108">DESCRIPTION</span></span>
<span data-ttu-id="873db-109">Polecenie cmdlet **Start-AzHpcCache** uruchamia pamięć podręczną usługi Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="873db-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="873db-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="873db-110">EXAMPLES</span></span>

### <span data-ttu-id="873db-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="873db-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="873db-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="873db-112">PARAMETERS</span></span>

### <span data-ttu-id="873db-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="873db-113">-AsJob</span></span>
<span data-ttu-id="873db-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="873db-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="873db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="873db-115">-DefaultProfile</span></span>
<span data-ttu-id="873db-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="873db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="873db-117">-Force</span><span class="sxs-lookup"><span data-stu-id="873db-117">-Force</span></span>
<span data-ttu-id="873db-118">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="873db-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="873db-119">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru uruchomienia pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="873db-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="873db-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="873db-120">-InputObject</span></span>
<span data-ttu-id="873db-121">Obiekt pamięci podręcznej, który ma zostać uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="873db-121">The cache object to start.</span></span>

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

### <span data-ttu-id="873db-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="873db-122">-Name</span></span>
<span data-ttu-id="873db-123">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="873db-123">Name of cache.</span></span>

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

### <span data-ttu-id="873db-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="873db-124">-PassThru</span></span>
<span data-ttu-id="873db-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="873db-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="873db-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="873db-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="873db-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="873db-127">-ResourceGroupName</span></span>
<span data-ttu-id="873db-128">Nazwa grupy zasobów, w której ma zostać rozpoczęta pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="873db-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="873db-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="873db-129">-ResourceId</span></span>
<span data-ttu-id="873db-130">Identyfikator zasobu w pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="873db-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="873db-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="873db-131">-Confirm</span></span>
<span data-ttu-id="873db-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="873db-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="873db-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="873db-133">-WhatIf</span></span>
<span data-ttu-id="873db-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="873db-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="873db-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="873db-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="873db-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="873db-136">CommonParameters</span></span>
<span data-ttu-id="873db-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="873db-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="873db-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="873db-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="873db-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="873db-139">INPUTS</span></span>

### <span data-ttu-id="873db-140">System. String</span><span class="sxs-lookup"><span data-stu-id="873db-140">System.String</span></span>

## <span data-ttu-id="873db-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="873db-141">OUTPUTS</span></span>

## <span data-ttu-id="873db-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="873db-142">NOTES</span></span>

## <span data-ttu-id="873db-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="873db-143">RELATED LINKS</span></span>
