---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 393f2a75217b95b6c1c5366326735ac0f78ac294
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868852"
---
# <span data-ttu-id="b11dd-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="b11dd-101">Stop-AzVM</span></span>

## <span data-ttu-id="b11dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b11dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b11dd-103">Zatrzymuje maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b11dd-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="b11dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b11dd-104">SYNTAX</span></span>

### <span data-ttu-id="b11dd-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b11dd-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b11dd-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b11dd-106">IdParameterSetName</span></span>
```
Stop-AzVM [[-Name] <String>] [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b11dd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b11dd-107">DESCRIPTION</span></span>
<span data-ttu-id="b11dd-108">Polecenie cmdlet **stop-AzVM** zatrzymuje maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b11dd-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="b11dd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b11dd-109">EXAMPLES</span></span>

### <span data-ttu-id="b11dd-110">Przykład 1: zatrzymywanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b11dd-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b11dd-111">To polecenie zatrzymuje maszynę wirtualną o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b11dd-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="b11dd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b11dd-112">PARAMETERS</span></span>

### <span data-ttu-id="b11dd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b11dd-113">-AsJob</span></span>
<span data-ttu-id="b11dd-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="b11dd-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b11dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b11dd-115">-DefaultProfile</span></span>
<span data-ttu-id="b11dd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b11dd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b11dd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b11dd-117">-Force</span></span>
<span data-ttu-id="b11dd-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b11dd-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b11dd-119">-ID</span><span class="sxs-lookup"><span data-stu-id="b11dd-119">-Id</span></span>
<span data-ttu-id="b11dd-120">Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b11dd-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="b11dd-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b11dd-121">-Name</span></span>
<span data-ttu-id="b11dd-122">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b11dd-122">The virtual machine name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b11dd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b11dd-123">-ResourceGroupName</span></span>
<span data-ttu-id="b11dd-124">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b11dd-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b11dd-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="b11dd-125">-StayProvisioned</span></span>
<span data-ttu-id="b11dd-126">Polecenie cmdlet zatrzymuje wszystkie maszyny wirtualne w VMSS, ale nie powoduje ich cofnięcia przydziału.</span><span class="sxs-lookup"><span data-stu-id="b11dd-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="b11dd-127">Konto jest obciążane za zatrzymane maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="b11dd-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="b11dd-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b11dd-128">-Confirm</span></span>
<span data-ttu-id="b11dd-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b11dd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b11dd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b11dd-130">-WhatIf</span></span>
<span data-ttu-id="b11dd-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b11dd-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b11dd-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b11dd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b11dd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b11dd-133">CommonParameters</span></span>
<span data-ttu-id="b11dd-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b11dd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b11dd-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b11dd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b11dd-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b11dd-136">INPUTS</span></span>

### <span data-ttu-id="b11dd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b11dd-137">System.String</span></span>

## <span data-ttu-id="b11dd-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b11dd-138">OUTPUTS</span></span>

### <span data-ttu-id="b11dd-139">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="b11dd-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="b11dd-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b11dd-140">NOTES</span></span>

## <span data-ttu-id="b11dd-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b11dd-141">RELATED LINKS</span></span>

[<span data-ttu-id="b11dd-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b11dd-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b11dd-143">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="b11dd-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="b11dd-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="b11dd-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="b11dd-145">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="b11dd-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="b11dd-146">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="b11dd-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="b11dd-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b11dd-147">Update-AzVM</span></span>](./Update-AzVM.md)


