---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: f87399901e00e19686d879799dbb799c7d79172c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553963"
---
# <span data-ttu-id="f2031-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="f2031-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="f2031-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2031-102">SYNOPSIS</span></span>
<span data-ttu-id="f2031-103">Anuluje bieżące uaktualnienie stopniowe zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f2031-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2031-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2031-104">SYNTAX</span></span>

### <span data-ttu-id="f2031-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f2031-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2031-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="f2031-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2031-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f2031-107">DESCRIPTION</span></span>
<span data-ttu-id="f2031-108">Anuluje bieżące uaktualnienie stopniowe zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f2031-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="f2031-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2031-109">EXAMPLES</span></span>

### <span data-ttu-id="f2031-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2031-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="f2031-111">To polecenie anuluje uaktualnianie stopniowe zestawu skali maszyny wirtualnej "VMSS001" w grupie zasobów "Group001".</span><span class="sxs-lookup"><span data-stu-id="f2031-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="f2031-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2031-112">PARAMETERS</span></span>

### <span data-ttu-id="f2031-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2031-113">-DefaultProfile</span></span>
<span data-ttu-id="f2031-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2031-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2031-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f2031-115">-Force</span></span>
<span data-ttu-id="f2031-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f2031-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f2031-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2031-117">-ResourceGroupName</span></span>
<span data-ttu-id="f2031-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2031-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2031-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f2031-119">-VMScaleSetName</span></span>
<span data-ttu-id="f2031-120">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f2031-120">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2031-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2031-121">-Confirm</span></span>
<span data-ttu-id="f2031-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2031-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2031-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2031-123">-WhatIf</span></span>
<span data-ttu-id="f2031-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2031-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2031-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f2031-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2031-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2031-126">CommonParameters</span></span>
<span data-ttu-id="f2031-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2031-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2031-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2031-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2031-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2031-129">INPUTS</span></span>

### <span data-ttu-id="f2031-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f2031-130">System.String</span></span>

## <span data-ttu-id="f2031-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2031-131">OUTPUTS</span></span>

### <span data-ttu-id="f2031-132">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f2031-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f2031-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2031-133">NOTES</span></span>

## <span data-ttu-id="f2031-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2031-134">RELATED LINKS</span></span>

