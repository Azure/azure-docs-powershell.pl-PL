---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 344f62f6114eb85e1a9e17b0e4d8c4da0acb93a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869059"
---
# <span data-ttu-id="18bfe-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="18bfe-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="18bfe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="18bfe-103">Przedstawia stan najnowszej aktualizacji stopniowej zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18bfe-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="18bfe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18bfe-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18bfe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="18bfe-105">DESCRIPTION</span></span>
<span data-ttu-id="18bfe-106">Przedstawia stan najnowszej aktualizacji stopniowej zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18bfe-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="18bfe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18bfe-107">EXAMPLES</span></span>

### <span data-ttu-id="18bfe-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="18bfe-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="18bfe-109">To polecenie wyświetla stan ostatniego uaktualnienia stopniowego VMSS o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="18bfe-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="18bfe-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18bfe-110">PARAMETERS</span></span>

### <span data-ttu-id="18bfe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18bfe-111">-DefaultProfile</span></span>
<span data-ttu-id="18bfe-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18bfe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18bfe-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18bfe-113">-ResourceGroupName</span></span>
<span data-ttu-id="18bfe-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="18bfe-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="18bfe-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="18bfe-115">-VMScaleSetName</span></span>
<span data-ttu-id="18bfe-116">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18bfe-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="18bfe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18bfe-117">CommonParameters</span></span>
<span data-ttu-id="18bfe-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18bfe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18bfe-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18bfe-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18bfe-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18bfe-120">INPUTS</span></span>

### <span data-ttu-id="18bfe-121">System. String</span><span class="sxs-lookup"><span data-stu-id="18bfe-121">System.String</span></span>

## <span data-ttu-id="18bfe-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18bfe-122">OUTPUTS</span></span>

### <span data-ttu-id="18bfe-123">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="18bfe-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="18bfe-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18bfe-124">NOTES</span></span>

## <span data-ttu-id="18bfe-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18bfe-125">RELATED LINKS</span></span>
