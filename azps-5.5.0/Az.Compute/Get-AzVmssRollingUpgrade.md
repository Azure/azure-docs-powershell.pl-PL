---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177714"
---
# <span data-ttu-id="f2320-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="f2320-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="f2320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2320-102">SYNOPSIS</span></span>
<span data-ttu-id="f2320-103">Pokazuje stan najnowszego zestawu skalowania maszyn wirtualnych, dla których jest uaktualnianie.</span><span class="sxs-lookup"><span data-stu-id="f2320-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="f2320-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f2320-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2320-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f2320-105">DESCRIPTION</span></span>
<span data-ttu-id="f2320-106">Pokazuje stan najnowszego zestawu skalowania maszyn wirtualnych, dla których jest uaktualnianie.</span><span class="sxs-lookup"><span data-stu-id="f2320-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="f2320-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f2320-107">EXAMPLES</span></span>

### <span data-ttu-id="f2320-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2320-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="f2320-109">To polecenie przedstawia stan najnowszego uaktualniania w celu uaktualnienia maszyn wirtualnych o nazwie VMSS001, które należy do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="f2320-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f2320-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2320-110">PARAMETERS</span></span>

### <span data-ttu-id="f2320-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2320-111">-DefaultProfile</span></span>
<span data-ttu-id="f2320-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2320-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2320-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2320-113">-ResourceGroupName</span></span>
<span data-ttu-id="f2320-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2320-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="f2320-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f2320-115">-VMScaleSetName</span></span>
<span data-ttu-id="f2320-116">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f2320-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="f2320-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2320-117">CommonParameters</span></span>
<span data-ttu-id="f2320-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2320-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2320-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2320-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2320-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2320-120">INPUTS</span></span>

### <span data-ttu-id="f2320-121">System.String</span><span class="sxs-lookup"><span data-stu-id="f2320-121">System.String</span></span>

## <span data-ttu-id="f2320-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2320-122">OUTPUTS</span></span>

### <span data-ttu-id="f2320-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="f2320-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="f2320-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f2320-124">NOTES</span></span>

## <span data-ttu-id="f2320-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2320-125">RELATED LINKS</span></span>
