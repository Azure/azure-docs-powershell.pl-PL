---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177467"
---
# <span data-ttu-id="a380e-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="a380e-101">Stop-AzVM</span></span>

## <span data-ttu-id="a380e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a380e-102">SYNOPSIS</span></span>
<span data-ttu-id="a380e-103">Zatrzymuje maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a380e-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="a380e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a380e-104">SYNTAX</span></span>

### <span data-ttu-id="a380e-105">ResourceGroupNameParameterSetName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="a380e-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a380e-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a380e-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a380e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a380e-107">DESCRIPTION</span></span>
<span data-ttu-id="a380e-108">Polecenie **cmdlet Stop-AzVM** zatrzymuje maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a380e-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="a380e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a380e-109">EXAMPLES</span></span>

### <span data-ttu-id="a380e-110">Przykład 1. Zatrzymywanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a380e-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="a380e-111">To polecenie zatrzymuje maszynę wirtualną o nazwie VirtualMachine07 w grupie Zasobów11.</span><span class="sxs-lookup"><span data-stu-id="a380e-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="a380e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a380e-112">PARAMETERS</span></span>

### <span data-ttu-id="a380e-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a380e-113">-AsJob</span></span>
<span data-ttu-id="a380e-114">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="a380e-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a380e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a380e-115">-DefaultProfile</span></span>
<span data-ttu-id="a380e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a380e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a380e-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a380e-117">-Force</span></span>
<span data-ttu-id="a380e-118">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a380e-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a380e-119">— Id</span><span class="sxs-lookup"><span data-stu-id="a380e-119">-Id</span></span>
<span data-ttu-id="a380e-120">Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a380e-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="a380e-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a380e-121">-Name</span></span>
<span data-ttu-id="a380e-122">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a380e-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a380e-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a380e-123">-NoWait</span></span>
<span data-ttu-id="a380e-124">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="a380e-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a380e-125">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="a380e-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a380e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a380e-126">-ResourceGroupName</span></span>
<span data-ttu-id="a380e-127">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a380e-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a380e-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="a380e-128">-SkipShutdown</span></span>
<span data-ttu-id="a380e-129">Aby zażądać bezbłędnego zamykania maszyny wirtualnej przy zachowaniu obsługi administracyjnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a380e-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="a380e-130">- StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="a380e-130">-StayProvisioned</span></span>
<span data-ttu-id="a380e-131">Polecenie cmdlet zatrzymuje wszystkie maszyny wirtualne w ramach maszyny wirtualnej, ale ich nie deallocate.</span><span class="sxs-lookup"><span data-stu-id="a380e-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="a380e-132">Opłata za zatrzymane maszyny wirtualne zostanie pobrana z konta.</span><span class="sxs-lookup"><span data-stu-id="a380e-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="a380e-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a380e-133">-Confirm</span></span>
<span data-ttu-id="a380e-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a380e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a380e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a380e-135">-WhatIf</span></span>
<span data-ttu-id="a380e-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a380e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a380e-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a380e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a380e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a380e-138">CommonParameters</span></span>
<span data-ttu-id="a380e-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a380e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a380e-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a380e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a380e-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a380e-141">INPUTS</span></span>

### <span data-ttu-id="a380e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a380e-142">System.String</span></span>

## <span data-ttu-id="a380e-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a380e-143">OUTPUTS</span></span>

### <span data-ttu-id="a380e-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a380e-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="a380e-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a380e-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a380e-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a380e-146">NOTES</span></span>

## <span data-ttu-id="a380e-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a380e-147">RELATED LINKS</span></span>

[<span data-ttu-id="a380e-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a380e-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a380e-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a380e-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="a380e-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="a380e-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="a380e-151">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="a380e-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="a380e-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="a380e-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="a380e-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a380e-153">Update-AzVM</span></span>](./Update-AzVM.md)


