---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: e87c307592f4487de239245ef06a70ea084ef916
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957633"
---
# <span data-ttu-id="b2fa9-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="b2fa9-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="b2fa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="b2fa9-103">Pokazuje stan najnowszego zestawu skalowania maszyn wirtualnych, dla których jest uaktualnianie.</span><span class="sxs-lookup"><span data-stu-id="b2fa9-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="b2fa9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b2fa9-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2fa9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b2fa9-105">DESCRIPTION</span></span>
<span data-ttu-id="b2fa9-106">Pokazuje stan najnowszego zestawu skalowania maszyn wirtualnych, dla których jest uaktualnianie.</span><span class="sxs-lookup"><span data-stu-id="b2fa9-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="b2fa9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b2fa9-107">EXAMPLES</span></span>

### <span data-ttu-id="b2fa9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2fa9-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="b2fa9-109">To polecenie przedstawia stan najnowszego uaktualniania w celu uaktualnienia w sposób toczący się maszyny wirtualnej o nazwie MASZYNY WIRTUALNE.S001, która należy do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="b2fa9-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="b2fa9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2fa9-110">PARAMETERS</span></span>

### <span data-ttu-id="b2fa9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2fa9-111">-DefaultProfile</span></span>
<span data-ttu-id="b2fa9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2fa9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2fa9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2fa9-113">-ResourceGroupName</span></span>
<span data-ttu-id="b2fa9-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2fa9-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="b2fa9-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b2fa9-115">-VMScaleSetName</span></span>
<span data-ttu-id="b2fa9-116">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b2fa9-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="b2fa9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2fa9-117">CommonParameters</span></span>
<span data-ttu-id="b2fa9-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2fa9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2fa9-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2fa9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2fa9-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2fa9-120">INPUTS</span></span>

### <span data-ttu-id="b2fa9-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b2fa9-121">System.String</span></span>

## <span data-ttu-id="b2fa9-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2fa9-122">OUTPUTS</span></span>

### <span data-ttu-id="b2fa9-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="b2fa9-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="b2fa9-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b2fa9-124">NOTES</span></span>

## <span data-ttu-id="b2fa9-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2fa9-125">RELATED LINKS</span></span>
