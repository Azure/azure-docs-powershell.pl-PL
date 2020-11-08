---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
ms.openlocfilehash: 5ccaccdc5d447ac9ccdc49cf53230c58a5758e4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220145"
---
# <span data-ttu-id="e76a4-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="e76a4-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="e76a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e76a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e76a4-103">Ocenianie stanu poprawki maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e76a4-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="e76a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e76a4-104">SYNTAX</span></span>

### <span data-ttu-id="e76a4-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e76a4-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e76a4-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="e76a4-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e76a4-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e76a4-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e76a4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e76a4-108">DESCRIPTION</span></span>
<span data-ttu-id="e76a4-109">Ocenia stan poprawki maszyny wirtualnej i wyświetla wszystkie wykryte poprawki, które są dostępne do zainstalowania.</span><span class="sxs-lookup"><span data-stu-id="e76a4-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="e76a4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e76a4-110">EXAMPLES</span></span>

### <span data-ttu-id="e76a4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e76a4-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="e76a4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e76a4-112">PARAMETERS</span></span>

### <span data-ttu-id="e76a4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e76a4-113">-AsJob</span></span>
<span data-ttu-id="e76a4-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e76a4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e76a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e76a4-115">-DefaultProfile</span></span>
<span data-ttu-id="e76a4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e76a4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e76a4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e76a4-117">-ResourceGroupName</span></span>
<span data-ttu-id="e76a4-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e76a4-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e76a4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e76a4-119">-ResourceId</span></span>
<span data-ttu-id="e76a4-120">Identyfikator zasobu dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e76a4-120">Resource ID for your virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e76a4-121">-VM</span><span class="sxs-lookup"><span data-stu-id="e76a4-121">-VM</span></span>
<span data-ttu-id="e76a4-122">Obiekt maszyny wirtualnej programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="e76a4-122">PowerShell Virtual Machine Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: InputObjectParameterSet
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e76a4-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="e76a4-123">-VMName</span></span>
<span data-ttu-id="e76a4-124">Nazwa maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e76a4-124">Virtual Machine name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e76a4-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e76a4-125">-Confirm</span></span>
<span data-ttu-id="e76a4-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e76a4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e76a4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e76a4-127">-WhatIf</span></span>
<span data-ttu-id="e76a4-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e76a4-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e76a4-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e76a4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e76a4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e76a4-130">CommonParameters</span></span>
<span data-ttu-id="e76a4-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e76a4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e76a4-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e76a4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e76a4-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e76a4-133">INPUTS</span></span>

### <span data-ttu-id="e76a4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e76a4-134">System.String</span></span>

## <span data-ttu-id="e76a4-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e76a4-135">OUTPUTS</span></span>

### <span data-ttu-id="e76a4-136">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="e76a4-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="e76a4-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e76a4-137">NOTES</span></span>

## <span data-ttu-id="e76a4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e76a4-138">RELATED LINKS</span></span>
