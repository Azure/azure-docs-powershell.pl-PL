---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
ms.openlocfilehash: 52e7a7372372bfcb0dfc93a9a89715e91c484b73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195034"
---
# <span data-ttu-id="77441-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="77441-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="77441-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77441-102">SYNOPSIS</span></span>
<span data-ttu-id="77441-103">Oceń stan poprawek na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="77441-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="77441-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="77441-104">SYNTAX</span></span>

### <span data-ttu-id="77441-105">DefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="77441-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77441-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="77441-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77441-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77441-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77441-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="77441-108">DESCRIPTION</span></span>
<span data-ttu-id="77441-109">Ocenia stan poprawek maszyny wirtualnej i raportuje wszystkie wykryte poprawki, które są dostępne do zainstalowania.</span><span class="sxs-lookup"><span data-stu-id="77441-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="77441-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="77441-110">EXAMPLES</span></span>

### <span data-ttu-id="77441-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77441-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="77441-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77441-112">PARAMETERS</span></span>

### <span data-ttu-id="77441-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="77441-113">-AsJob</span></span>
<span data-ttu-id="77441-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="77441-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77441-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77441-115">-DefaultProfile</span></span>
<span data-ttu-id="77441-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="77441-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77441-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77441-117">-ResourceGroupName</span></span>
<span data-ttu-id="77441-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="77441-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="77441-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77441-119">-ResourceId</span></span>
<span data-ttu-id="77441-120">Identyfikator zasobu dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="77441-120">Resource ID for your virtual machine.</span></span>

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

### <span data-ttu-id="77441-121">— MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="77441-121">-VM</span></span>
<span data-ttu-id="77441-122">Obiekt maszyny wirtualnej programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="77441-122">PowerShell Virtual Machine Object</span></span>

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

### <span data-ttu-id="77441-123">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="77441-123">-VMName</span></span>
<span data-ttu-id="77441-124">Nazwa maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="77441-124">Virtual Machine name</span></span>

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

### <span data-ttu-id="77441-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77441-125">-Confirm</span></span>
<span data-ttu-id="77441-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="77441-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77441-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77441-127">-WhatIf</span></span>
<span data-ttu-id="77441-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77441-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77441-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="77441-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77441-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77441-130">CommonParameters</span></span>
<span data-ttu-id="77441-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77441-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77441-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77441-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77441-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77441-133">INPUTS</span></span>

### <span data-ttu-id="77441-134">System.String</span><span class="sxs-lookup"><span data-stu-id="77441-134">System.String</span></span>

## <span data-ttu-id="77441-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77441-135">OUTPUTS</span></span>

### <span data-ttu-id="77441-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="77441-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="77441-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="77441-137">NOTES</span></span>

## <span data-ttu-id="77441-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77441-138">RELATED LINKS</span></span>
