---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: 292da4caf90fb43895ec5cda12dcfc6418e6bde9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552972"
---
# <span data-ttu-id="dcefe-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="dcefe-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="dcefe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcefe-102">SYNOPSIS</span></span>
<span data-ttu-id="dcefe-103">Anuluje bieżące uaktualnienie stopniowe zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dcefe-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcefe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcefe-104">SYNTAX</span></span>

### <span data-ttu-id="dcefe-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dcefe-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcefe-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="dcefe-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcefe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dcefe-107">DESCRIPTION</span></span>
<span data-ttu-id="dcefe-108">Anuluje bieżące uaktualnienie stopniowe zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dcefe-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="dcefe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcefe-109">EXAMPLES</span></span>

### <span data-ttu-id="dcefe-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dcefe-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="dcefe-111">To polecenie anuluje uaktualnianie stopniowe zestawu skali maszyny wirtualnej "VMSS001" w grupie zasobów "Group001".</span><span class="sxs-lookup"><span data-stu-id="dcefe-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="dcefe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcefe-112">PARAMETERS</span></span>

### <span data-ttu-id="dcefe-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcefe-113">-AsJob</span></span>
<span data-ttu-id="dcefe-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="dcefe-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcefe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcefe-115">-DefaultProfile</span></span>
<span data-ttu-id="dcefe-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcefe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcefe-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dcefe-117">-Force</span></span>
<span data-ttu-id="dcefe-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dcefe-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dcefe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcefe-119">-ResourceGroupName</span></span>
<span data-ttu-id="dcefe-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dcefe-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="dcefe-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="dcefe-121">-VMScaleSetName</span></span>
<span data-ttu-id="dcefe-122">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dcefe-122">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="dcefe-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dcefe-123">-Confirm</span></span>
<span data-ttu-id="dcefe-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcefe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcefe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcefe-125">-WhatIf</span></span>
<span data-ttu-id="dcefe-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcefe-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcefe-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dcefe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcefe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcefe-128">CommonParameters</span></span>
<span data-ttu-id="dcefe-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcefe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcefe-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcefe-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcefe-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcefe-131">INPUTS</span></span>

### <span data-ttu-id="dcefe-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dcefe-132">System.String</span></span>

## <span data-ttu-id="dcefe-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcefe-133">OUTPUTS</span></span>

### <span data-ttu-id="dcefe-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="dcefe-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="dcefe-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcefe-135">NOTES</span></span>

## <span data-ttu-id="dcefe-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcefe-136">RELATED LINKS</span></span>
