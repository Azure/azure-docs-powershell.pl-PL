---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328202"
---
# <span data-ttu-id="d1657-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="d1657-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="d1657-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1657-102">SYNOPSIS</span></span>
<span data-ttu-id="d1657-103">Aktualizuje znaczniki w pamięci podręcznej HPC.</span><span class="sxs-lookup"><span data-stu-id="d1657-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="d1657-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1657-104">SYNTAX</span></span>

### <span data-ttu-id="d1657-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d1657-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1657-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1657-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1657-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d1657-107">DESCRIPTION</span></span>
<span data-ttu-id="d1657-108">Polecenie cmdlet **Set-AzHpcCache** aktualizuje znaczniki pamięci podręcznej platformy Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="d1657-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="d1657-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1657-109">EXAMPLES</span></span>

### <span data-ttu-id="d1657-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d1657-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="d1657-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1657-111">PARAMETERS</span></span>

### <span data-ttu-id="d1657-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1657-112">-AsJob</span></span>
<span data-ttu-id="d1657-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d1657-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1657-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1657-114">-DefaultProfile</span></span>
<span data-ttu-id="d1657-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1657-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1657-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d1657-116">-InputObject</span></span>
<span data-ttu-id="d1657-117">Obiekt pamięci podręcznej do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="d1657-117">The cache object to update.</span></span>

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

### <span data-ttu-id="d1657-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1657-118">-Name</span></span>
<span data-ttu-id="d1657-119">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="d1657-119">Name of cache.</span></span>

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

### <span data-ttu-id="d1657-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1657-120">-ResourceGroupName</span></span>
<span data-ttu-id="d1657-121">Nazwa grupy zasobów, pod którą ma zostać zaktualizowana pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="d1657-121">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="d1657-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1657-122">-Tag</span></span>
<span data-ttu-id="d1657-123">Znaczniki, które mają zostać skojarzone z pamięcią podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="d1657-123">The tags to associate with HPC Cache.</span></span> 

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

### <span data-ttu-id="d1657-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1657-124">-Confirm</span></span>
<span data-ttu-id="d1657-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1657-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1657-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1657-126">-WhatIf</span></span>
<span data-ttu-id="d1657-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1657-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1657-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d1657-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1657-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1657-129">CommonParameters</span></span>
<span data-ttu-id="d1657-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1657-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1657-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1657-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1657-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1657-132">INPUTS</span></span>

### <span data-ttu-id="d1657-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d1657-133">System.String</span></span>

### <span data-ttu-id="d1657-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d1657-134">System.Int32</span></span>

## <span data-ttu-id="d1657-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1657-135">OUTPUTS</span></span>

### <span data-ttu-id="d1657-136">Microsoft. Azure. PowerShell. polecenia. HPCCache. models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="d1657-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="d1657-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1657-137">NOTES</span></span>

## <span data-ttu-id="d1657-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1657-138">RELATED LINKS</span></span>
