---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: cbe44db07cbf32195f92ebefc0a2032a5f288a1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706139"
---
# <span data-ttu-id="ca01c-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="ca01c-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="ca01c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca01c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca01c-103">Anuluje bieżące uaktualnienie stopniowe zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ca01c-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="ca01c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca01c-104">SYNTAX</span></span>

### <span data-ttu-id="ca01c-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ca01c-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca01c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ca01c-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca01c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ca01c-107">DESCRIPTION</span></span>
<span data-ttu-id="ca01c-108">Anuluje bieżące uaktualnienie stopniowe zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ca01c-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="ca01c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca01c-109">EXAMPLES</span></span>

### <span data-ttu-id="ca01c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca01c-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="ca01c-111">To polecenie anuluje uaktualnianie stopniowe zestawu skali maszyny wirtualnej "VMSS001" w grupie zasobów "Group001".</span><span class="sxs-lookup"><span data-stu-id="ca01c-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="ca01c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca01c-112">PARAMETERS</span></span>

### <span data-ttu-id="ca01c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca01c-113">-AsJob</span></span>
<span data-ttu-id="ca01c-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ca01c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca01c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca01c-115">-DefaultProfile</span></span>
<span data-ttu-id="ca01c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca01c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca01c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ca01c-117">-Force</span></span>
<span data-ttu-id="ca01c-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ca01c-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ca01c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca01c-119">-ResourceGroupName</span></span>
<span data-ttu-id="ca01c-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca01c-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca01c-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ca01c-121">-VMScaleSetName</span></span>
<span data-ttu-id="ca01c-122">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ca01c-122">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca01c-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca01c-123">-Confirm</span></span>
<span data-ttu-id="ca01c-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca01c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca01c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca01c-125">-WhatIf</span></span>
<span data-ttu-id="ca01c-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca01c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca01c-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca01c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca01c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca01c-128">CommonParameters</span></span>
<span data-ttu-id="ca01c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca01c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca01c-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca01c-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca01c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca01c-131">INPUTS</span></span>

### <span data-ttu-id="ca01c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ca01c-132">System.String</span></span>

## <span data-ttu-id="ca01c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca01c-133">OUTPUTS</span></span>

### <span data-ttu-id="ca01c-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ca01c-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ca01c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca01c-135">NOTES</span></span>

## <span data-ttu-id="ca01c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca01c-136">RELATED LINKS</span></span>
