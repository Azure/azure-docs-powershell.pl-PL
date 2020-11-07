---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: 9d54e769686f7106ce2f0f0b2dea755c1f8e1155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717863"
---
# <span data-ttu-id="5dccb-101">Get-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="5dccb-101">Get-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="5dccb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5dccb-102">SYNOPSIS</span></span>
<span data-ttu-id="5dccb-103">Przedstawia stan najnowszej aktualizacji stopniowej zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5dccb-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dccb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5dccb-104">SYNTAX</span></span>

```
Get-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dccb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5dccb-105">DESCRIPTION</span></span>
<span data-ttu-id="5dccb-106">Przedstawia stan najnowszej aktualizacji stopniowej zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5dccb-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="5dccb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5dccb-107">EXAMPLES</span></span>

### <span data-ttu-id="5dccb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5dccb-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="5dccb-109">To polecenie wyświetla stan ostatniego uaktualnienia stopniowego VMSS o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="5dccb-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="5dccb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5dccb-110">PARAMETERS</span></span>

### <span data-ttu-id="5dccb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dccb-111">-DefaultProfile</span></span>
<span data-ttu-id="5dccb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5dccb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dccb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dccb-113">-ResourceGroupName</span></span>
<span data-ttu-id="5dccb-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5dccb-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dccb-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5dccb-115">-VMScaleSetName</span></span>
<span data-ttu-id="5dccb-116">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5dccb-116">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dccb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dccb-117">CommonParameters</span></span>
<span data-ttu-id="5dccb-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dccb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dccb-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dccb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dccb-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5dccb-120">INPUTS</span></span>

### <span data-ttu-id="5dccb-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5dccb-121">System.String</span></span>

## <span data-ttu-id="5dccb-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5dccb-122">OUTPUTS</span></span>

### <span data-ttu-id="5dccb-123">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="5dccb-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="5dccb-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5dccb-124">NOTES</span></span>

## <span data-ttu-id="5dccb-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5dccb-125">RELATED LINKS</span></span>
