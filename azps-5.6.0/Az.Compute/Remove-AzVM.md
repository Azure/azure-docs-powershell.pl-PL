---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: d5ce1af197575f96fd21f5355c0edfb98e3b181f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978769"
---
# <span data-ttu-id="a75b4-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="a75b4-101">Remove-AzVM</span></span>

## <span data-ttu-id="a75b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a75b4-102">SYNOPSIS</span></span>
<span data-ttu-id="a75b4-103">Usuwa maszynę wirtualną z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a75b4-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="a75b4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a75b4-104">SYNTAX</span></span>

### <span data-ttu-id="a75b4-105">ResourceGroupNameParameterSetName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="a75b4-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a75b4-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a75b4-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a75b4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a75b4-107">DESCRIPTION</span></span>
<span data-ttu-id="a75b4-108">Polecenie **cmdlet Remove-AzVM** usuwa maszynę wirtualną z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a75b4-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="a75b4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a75b4-109">EXAMPLES</span></span>

### <span data-ttu-id="a75b4-110">Przykład 1. Usuwanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a75b4-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="a75b4-111">To polecenie usuwa maszynę wirtualną o nazwie VirtualMachine07 z grupy zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a75b4-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="a75b4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a75b4-112">PARAMETERS</span></span>

### <span data-ttu-id="a75b4-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a75b4-113">-AsJob</span></span>
<span data-ttu-id="a75b4-114">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="a75b4-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a75b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a75b4-115">-DefaultProfile</span></span>
<span data-ttu-id="a75b4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a75b4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a75b4-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a75b4-117">-Force</span></span>
<span data-ttu-id="a75b4-118">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a75b4-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75b4-119">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="a75b4-119">-Id</span></span>
<span data-ttu-id="a75b4-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a75b4-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a75b4-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a75b4-121">-Name</span></span>
<span data-ttu-id="a75b4-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a75b4-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a75b4-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a75b4-123">-NoWait</span></span>
<span data-ttu-id="a75b4-124">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="a75b4-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a75b4-125">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="a75b4-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a75b4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a75b4-126">-ResourceGroupName</span></span>
<span data-ttu-id="a75b4-127">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a75b4-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a75b4-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a75b4-128">-Confirm</span></span>
<span data-ttu-id="a75b4-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a75b4-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75b4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a75b4-130">-WhatIf</span></span>
<span data-ttu-id="a75b4-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a75b4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a75b4-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a75b4-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75b4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a75b4-133">CommonParameters</span></span>
<span data-ttu-id="a75b4-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a75b4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a75b4-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a75b4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a75b4-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a75b4-136">INPUTS</span></span>

### <span data-ttu-id="a75b4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a75b4-137">System.String</span></span>

## <span data-ttu-id="a75b4-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a75b4-138">OUTPUTS</span></span>

### <span data-ttu-id="a75b4-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a75b4-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="a75b4-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a75b4-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a75b4-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a75b4-141">NOTES</span></span>

## <span data-ttu-id="a75b4-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a75b4-142">RELATED LINKS</span></span>

[<span data-ttu-id="a75b4-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a75b4-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a75b4-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a75b4-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="a75b4-145">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="a75b4-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="a75b4-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="a75b4-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="a75b4-147">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="a75b4-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="a75b4-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a75b4-148">Update-AzVM</span></span>](./Update-AzVM.md)


