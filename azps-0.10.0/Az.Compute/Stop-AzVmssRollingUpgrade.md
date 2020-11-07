---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 915dd31b522fdbc7955494c0f76d69ee5a4b8376
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891606"
---
# <span data-ttu-id="15874-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="15874-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="15874-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15874-102">SYNOPSIS</span></span>
<span data-ttu-id="15874-103">Anuluje bieżące uaktualnienie stopniowe zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="15874-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="15874-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15874-104">SYNTAX</span></span>

### <span data-ttu-id="15874-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="15874-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15874-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="15874-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15874-107">Opis</span><span class="sxs-lookup"><span data-stu-id="15874-107">DESCRIPTION</span></span>
<span data-ttu-id="15874-108">Anuluje bieżące uaktualnienie stopniowe zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="15874-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="15874-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15874-109">EXAMPLES</span></span>

### <span data-ttu-id="15874-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="15874-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="15874-111">To polecenie anuluje uaktualnianie stopniowe zestawu skali maszyny wirtualnej "VMSS001" w grupie zasobów "Group001".</span><span class="sxs-lookup"><span data-stu-id="15874-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="15874-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15874-112">PARAMETERS</span></span>

### <span data-ttu-id="15874-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15874-113">-AsJob</span></span>
<span data-ttu-id="15874-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="15874-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15874-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15874-115">-DefaultProfile</span></span>
<span data-ttu-id="15874-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15874-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15874-117">-Force</span><span class="sxs-lookup"><span data-stu-id="15874-117">-Force</span></span>
<span data-ttu-id="15874-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="15874-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="15874-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15874-119">-ResourceGroupName</span></span>
<span data-ttu-id="15874-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="15874-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="15874-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="15874-121">-VMScaleSetName</span></span>
<span data-ttu-id="15874-122">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="15874-122">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="15874-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15874-123">-Confirm</span></span>
<span data-ttu-id="15874-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15874-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15874-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15874-125">-WhatIf</span></span>
<span data-ttu-id="15874-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15874-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15874-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="15874-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15874-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15874-128">CommonParameters</span></span>
<span data-ttu-id="15874-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15874-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15874-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15874-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15874-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15874-131">INPUTS</span></span>

### <span data-ttu-id="15874-132">System. String</span><span class="sxs-lookup"><span data-stu-id="15874-132">System.String</span></span>

## <span data-ttu-id="15874-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15874-133">OUTPUTS</span></span>

### <span data-ttu-id="15874-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="15874-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="15874-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15874-135">NOTES</span></span>

## <span data-ttu-id="15874-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15874-136">RELATED LINKS</span></span>

