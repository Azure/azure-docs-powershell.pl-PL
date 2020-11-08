---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: 39e695ad33568ca88996428c3e3d972ae693b503
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222797"
---
# <span data-ttu-id="50758-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="50758-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="50758-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50758-102">SYNOPSIS</span></span>
<span data-ttu-id="50758-103">Wywołuje określone akcje w udziale.</span><span class="sxs-lookup"><span data-stu-id="50758-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="50758-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50758-104">SYNTAX</span></span>

### <span data-ttu-id="50758-105">InvokeByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="50758-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50758-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50758-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50758-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50758-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50758-108">Opis</span><span class="sxs-lookup"><span data-stu-id="50758-108">DESCRIPTION</span></span>
<span data-ttu-id="50758-109">Polecenie cmdlet **Invoke-AzStackEdgeShare** wywołuje akcję odświeżania danych w udziale na urządzeniu ze stosem.</span><span class="sxs-lookup"><span data-stu-id="50758-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="50758-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50758-110">EXAMPLES</span></span>

### <span data-ttu-id="50758-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="50758-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="50758-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="50758-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="50758-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50758-113">PARAMETERS</span></span>

### <span data-ttu-id="50758-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50758-114">-AsJob</span></span>
<span data-ttu-id="50758-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="50758-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50758-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50758-116">-DefaultProfile</span></span>
<span data-ttu-id="50758-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50758-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50758-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="50758-118">-DeviceName</span></span>
<span data-ttu-id="50758-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="50758-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50758-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="50758-120">-InputObject</span></span>
<span data-ttu-id="50758-121">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="50758-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50758-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50758-122">-Name</span></span>
<span data-ttu-id="50758-123">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="50758-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50758-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50758-124">-PassThru</span></span>
<span data-ttu-id="50758-125">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="50758-125">returns true if successful</span></span>

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

### <span data-ttu-id="50758-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="50758-126">-RefreshData</span></span>
<span data-ttu-id="50758-127">Odświeżanie metadanych udziału przy użyciu danych z chmury</span><span class="sxs-lookup"><span data-stu-id="50758-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="50758-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50758-128">-ResourceGroupName</span></span>
<span data-ttu-id="50758-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="50758-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50758-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50758-130">-ResourceId</span></span>
<span data-ttu-id="50758-131">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="50758-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50758-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50758-132">-Confirm</span></span>
<span data-ttu-id="50758-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50758-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50758-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50758-134">-WhatIf</span></span>
<span data-ttu-id="50758-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50758-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50758-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="50758-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50758-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50758-137">CommonParameters</span></span>
<span data-ttu-id="50758-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50758-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50758-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50758-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50758-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50758-140">INPUTS</span></span>

### <span data-ttu-id="50758-141">System. String</span><span class="sxs-lookup"><span data-stu-id="50758-141">System.String</span></span>

### <span data-ttu-id="50758-142">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="50758-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="50758-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50758-143">OUTPUTS</span></span>

### <span data-ttu-id="50758-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50758-144">System.Boolean</span></span>

## <span data-ttu-id="50758-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50758-145">NOTES</span></span>

## <span data-ttu-id="50758-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50758-146">RELATED LINKS</span></span>
