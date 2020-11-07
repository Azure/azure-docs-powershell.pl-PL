---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmssrollingupgrade
schema: 2.0.0
ms.openlocfilehash: 8893f5fc8f6bf798635fdfd5e9a16bc4179815e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899362"
---
# <span data-ttu-id="fe7aa-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="fe7aa-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="fe7aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe7aa-102">SYNOPSIS</span></span>
<span data-ttu-id="fe7aa-103">Anuluje bieżące uaktualnienie stopniowe zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fe7aa-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe7aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe7aa-104">SYNTAX</span></span>

### <span data-ttu-id="fe7aa-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fe7aa-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe7aa-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="fe7aa-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe7aa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fe7aa-107">DESCRIPTION</span></span>
<span data-ttu-id="fe7aa-108">Anuluje bieżące uaktualnienie stopniowe zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fe7aa-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="fe7aa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe7aa-109">EXAMPLES</span></span>

### <span data-ttu-id="fe7aa-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fe7aa-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="fe7aa-111">To polecenie anuluje uaktualnianie stopniowe zestawu skali maszyny wirtualnej "VMSS001" w grupie zasobów "Group001".</span><span class="sxs-lookup"><span data-stu-id="fe7aa-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="fe7aa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe7aa-112">PARAMETERS</span></span>

### <span data-ttu-id="fe7aa-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe7aa-113">-AsJob</span></span>
<span data-ttu-id="fe7aa-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fe7aa-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe7aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe7aa-115">-DefaultProfile</span></span>
<span data-ttu-id="fe7aa-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe7aa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe7aa-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fe7aa-117">-Force</span></span>
<span data-ttu-id="fe7aa-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fe7aa-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe7aa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe7aa-119">-ResourceGroupName</span></span>
<span data-ttu-id="fe7aa-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe7aa-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7aa-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fe7aa-121">-VMScaleSetName</span></span>
<span data-ttu-id="fe7aa-122">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fe7aa-122">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7aa-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe7aa-123">-Confirm</span></span>
<span data-ttu-id="fe7aa-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe7aa-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe7aa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe7aa-125">-WhatIf</span></span>
<span data-ttu-id="fe7aa-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe7aa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe7aa-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fe7aa-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe7aa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe7aa-128">CommonParameters</span></span>
<span data-ttu-id="fe7aa-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe7aa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe7aa-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe7aa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe7aa-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe7aa-131">INPUTS</span></span>

### <span data-ttu-id="fe7aa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fe7aa-132">System.String</span></span>

## <span data-ttu-id="fe7aa-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe7aa-133">OUTPUTS</span></span>

### <span data-ttu-id="fe7aa-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="fe7aa-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="fe7aa-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe7aa-135">NOTES</span></span>

## <span data-ttu-id="fe7aa-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe7aa-136">RELATED LINKS</span></span>

