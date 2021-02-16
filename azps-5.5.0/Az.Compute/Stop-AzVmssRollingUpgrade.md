---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177459"
---
# <span data-ttu-id="726d3-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="726d3-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="726d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="726d3-102">SYNOPSIS</span></span>
<span data-ttu-id="726d3-103">Anulowanie bieżącego zestawu skalowania maszyn wirtualnych, w przypadku których jest uaktualnianie.</span><span class="sxs-lookup"><span data-stu-id="726d3-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="726d3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="726d3-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="726d3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="726d3-105">DESCRIPTION</span></span>
<span data-ttu-id="726d3-106">Anulowanie bieżącego zestawu skalowania maszyn wirtualnych, które jest uaktualnianie.</span><span class="sxs-lookup"><span data-stu-id="726d3-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="726d3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="726d3-107">EXAMPLES</span></span>

### <span data-ttu-id="726d3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="726d3-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="726d3-109">To polecenie anuluje toczące się uaktualnianie zestawu skali maszyny wirtualnej "MASZYNY WIRTUALNE", który jest ustawiony jako "MASZYNY WIRTUALNE", w grupie zasobów "Group001".</span><span class="sxs-lookup"><span data-stu-id="726d3-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="726d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="726d3-110">PARAMETERS</span></span>

### <span data-ttu-id="726d3-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="726d3-111">-AsJob</span></span>
<span data-ttu-id="726d3-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="726d3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="726d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="726d3-113">-DefaultProfile</span></span>
<span data-ttu-id="726d3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="726d3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="726d3-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="726d3-115">-Force</span></span>
<span data-ttu-id="726d3-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="726d3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="726d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="726d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="726d3-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="726d3-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="726d3-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="726d3-119">-VMScaleSetName</span></span>
<span data-ttu-id="726d3-120">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="726d3-120">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="726d3-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="726d3-121">-Confirm</span></span>
<span data-ttu-id="726d3-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="726d3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="726d3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="726d3-123">-WhatIf</span></span>
<span data-ttu-id="726d3-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="726d3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="726d3-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="726d3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="726d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="726d3-126">CommonParameters</span></span>
<span data-ttu-id="726d3-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="726d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="726d3-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="726d3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="726d3-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="726d3-129">INPUTS</span></span>

### <span data-ttu-id="726d3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="726d3-130">System.String</span></span>

## <span data-ttu-id="726d3-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="726d3-131">OUTPUTS</span></span>

### <span data-ttu-id="726d3-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="726d3-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="726d3-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="726d3-133">NOTES</span></span>

## <span data-ttu-id="726d3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="726d3-134">RELATED LINKS</span></span>
