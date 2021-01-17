---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 6e733bfecea9a054bbab3794ca61778894c613fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346318"
---
# <span data-ttu-id="49823-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="49823-101">Remove-AzVM</span></span>

## <span data-ttu-id="49823-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49823-102">SYNOPSIS</span></span>
<span data-ttu-id="49823-103">Umożliwia usunięcie maszyny wirtualnej z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="49823-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="49823-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49823-104">SYNTAX</span></span>

### <span data-ttu-id="49823-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="49823-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49823-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="49823-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49823-107">Opis</span><span class="sxs-lookup"><span data-stu-id="49823-107">DESCRIPTION</span></span>
<span data-ttu-id="49823-108">Polecenie cmdlet **Remove-AzVM** umożliwia usunięcie maszyny wirtualnej z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="49823-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="49823-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49823-109">EXAMPLES</span></span>

### <span data-ttu-id="49823-110">Przykład 1: usuwanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="49823-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="49823-111">To polecenie powoduje usunięcie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49823-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="49823-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49823-112">PARAMETERS</span></span>

### <span data-ttu-id="49823-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49823-113">-AsJob</span></span>
<span data-ttu-id="49823-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="49823-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="49823-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49823-115">-DefaultProfile</span></span>
<span data-ttu-id="49823-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49823-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49823-117">-Force</span><span class="sxs-lookup"><span data-stu-id="49823-117">-Force</span></span>
<span data-ttu-id="49823-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="49823-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="49823-119">-ID</span><span class="sxs-lookup"><span data-stu-id="49823-119">-Id</span></span>
<span data-ttu-id="49823-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49823-120">The resource group name.</span></span>

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

### <span data-ttu-id="49823-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="49823-121">-Name</span></span>
<span data-ttu-id="49823-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="49823-122">The resource name.</span></span>

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

### <span data-ttu-id="49823-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="49823-123">-NoWait</span></span>
<span data-ttu-id="49823-124">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="49823-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="49823-125">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="49823-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="49823-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49823-126">-ResourceGroupName</span></span>
<span data-ttu-id="49823-127">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49823-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="49823-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49823-128">-Confirm</span></span>
<span data-ttu-id="49823-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49823-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49823-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49823-130">-WhatIf</span></span>
<span data-ttu-id="49823-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49823-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49823-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49823-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49823-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49823-133">CommonParameters</span></span>
<span data-ttu-id="49823-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49823-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49823-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49823-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49823-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49823-136">INPUTS</span></span>

### <span data-ttu-id="49823-137">System. String</span><span class="sxs-lookup"><span data-stu-id="49823-137">System.String</span></span>

## <span data-ttu-id="49823-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49823-138">OUTPUTS</span></span>

### <span data-ttu-id="49823-139">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="49823-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="49823-140">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="49823-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="49823-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49823-141">NOTES</span></span>

## <span data-ttu-id="49823-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49823-142">RELATED LINKS</span></span>

[<span data-ttu-id="49823-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="49823-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="49823-144">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="49823-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="49823-145">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="49823-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="49823-146">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="49823-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="49823-147">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="49823-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="49823-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="49823-148">Update-AzVM</span></span>](./Update-AzVM.md)


