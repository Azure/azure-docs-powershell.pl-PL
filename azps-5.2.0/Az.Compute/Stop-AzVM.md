---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347233"
---
# <span data-ttu-id="60123-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="60123-101">Stop-AzVM</span></span>

## <span data-ttu-id="60123-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60123-102">SYNOPSIS</span></span>
<span data-ttu-id="60123-103">Zatrzymuje maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="60123-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="60123-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60123-104">SYNTAX</span></span>

### <span data-ttu-id="60123-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="60123-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60123-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="60123-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60123-107">Opis</span><span class="sxs-lookup"><span data-stu-id="60123-107">DESCRIPTION</span></span>
<span data-ttu-id="60123-108">Polecenie cmdlet **stop-AzVM** zatrzymuje maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="60123-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="60123-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60123-109">EXAMPLES</span></span>

### <span data-ttu-id="60123-110">Przykład 1: zatrzymywanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="60123-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="60123-111">To polecenie zatrzymuje maszynę wirtualną o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="60123-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="60123-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60123-112">PARAMETERS</span></span>

### <span data-ttu-id="60123-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60123-113">-AsJob</span></span>
<span data-ttu-id="60123-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="60123-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="60123-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60123-115">-DefaultProfile</span></span>
<span data-ttu-id="60123-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60123-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60123-117">-Force</span><span class="sxs-lookup"><span data-stu-id="60123-117">-Force</span></span>
<span data-ttu-id="60123-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="60123-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="60123-119">-ID</span><span class="sxs-lookup"><span data-stu-id="60123-119">-Id</span></span>
<span data-ttu-id="60123-120">Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="60123-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="60123-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="60123-121">-Name</span></span>
<span data-ttu-id="60123-122">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="60123-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="60123-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="60123-123">-NoWait</span></span>
<span data-ttu-id="60123-124">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="60123-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="60123-125">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="60123-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="60123-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60123-126">-ResourceGroupName</span></span>
<span data-ttu-id="60123-127">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="60123-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="60123-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="60123-128">-SkipShutdown</span></span>
<span data-ttu-id="60123-129">Aby zażądać niebezpiecznego zamknięcia maszyny wirtualnej podczas zachowywania obsługi maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="60123-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="60123-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="60123-130">-StayProvisioned</span></span>
<span data-ttu-id="60123-131">Polecenie cmdlet zatrzymuje wszystkie maszyny wirtualne w VMSS, ale nie powoduje ich cofnięcia przydziału.</span><span class="sxs-lookup"><span data-stu-id="60123-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="60123-132">Konto jest obciążane za zatrzymane maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="60123-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="60123-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60123-133">-Confirm</span></span>
<span data-ttu-id="60123-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60123-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60123-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60123-135">-WhatIf</span></span>
<span data-ttu-id="60123-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60123-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60123-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="60123-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60123-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60123-138">CommonParameters</span></span>
<span data-ttu-id="60123-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60123-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60123-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60123-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60123-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60123-141">INPUTS</span></span>

### <span data-ttu-id="60123-142">System. String</span><span class="sxs-lookup"><span data-stu-id="60123-142">System.String</span></span>

## <span data-ttu-id="60123-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60123-143">OUTPUTS</span></span>

### <span data-ttu-id="60123-144">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="60123-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="60123-145">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="60123-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="60123-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60123-146">NOTES</span></span>

## <span data-ttu-id="60123-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60123-147">RELATED LINKS</span></span>

[<span data-ttu-id="60123-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="60123-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="60123-149">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="60123-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="60123-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="60123-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="60123-151">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="60123-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="60123-152">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="60123-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="60123-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="60123-153">Update-AzVM</span></span>](./Update-AzVM.md)


