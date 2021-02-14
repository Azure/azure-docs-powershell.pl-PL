---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244051"
---
# <span data-ttu-id="91cc7-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="91cc7-101">Set-AzVM</span></span>

## <span data-ttu-id="91cc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="91cc7-103">Oznacza maszynę wirtualną jako uogólniona.</span><span class="sxs-lookup"><span data-stu-id="91cc7-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="91cc7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="91cc7-104">SYNTAX</span></span>

### <span data-ttu-id="91cc7-105">GeneralizeResourceGroupNameParameterSetName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="91cc7-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91cc7-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="91cc7-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91cc7-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="91cc7-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91cc7-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="91cc7-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91cc7-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="91cc7-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91cc7-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="91cc7-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91cc7-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="91cc7-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91cc7-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="91cc7-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91cc7-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="91cc7-113">DESCRIPTION</span></span>
<span data-ttu-id="91cc7-114">Polecenie **cmdlet Set-AzVM** oznacza maszynę wirtualną jako uogólnione.</span><span class="sxs-lookup"><span data-stu-id="91cc7-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="91cc7-115">Przed uruchomieniem tego polecenia cmdlet zaloguj się do maszyny wirtualnej i przygotuj dysk twardy za pomocą narzędzia Sysprep.</span><span class="sxs-lookup"><span data-stu-id="91cc7-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="91cc7-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="91cc7-116">EXAMPLES</span></span>

### <span data-ttu-id="91cc7-117">Przykład 1. Oznaczenie maszyny wirtualnej jako uogólnionych</span><span class="sxs-lookup"><span data-stu-id="91cc7-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="91cc7-118">To polecenie oznacza komputer wirtualny o nazwie VirtualMachine07 jako uogólniony.</span><span class="sxs-lookup"><span data-stu-id="91cc7-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="91cc7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91cc7-119">PARAMETERS</span></span>

### <span data-ttu-id="91cc7-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="91cc7-120">-AsJob</span></span>
<span data-ttu-id="91cc7-121">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="91cc7-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="91cc7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91cc7-122">-DefaultProfile</span></span>
<span data-ttu-id="91cc7-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="91cc7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91cc7-124">- Uogólnione</span><span class="sxs-lookup"><span data-stu-id="91cc7-124">-Generalized</span></span>
<span data-ttu-id="91cc7-125">Wskazuje, że to polecenie cmdlet oznacza maszynę wirtualną jako uogólnione.</span><span class="sxs-lookup"><span data-stu-id="91cc7-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91cc7-126">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="91cc7-126">-Id</span></span>
<span data-ttu-id="91cc7-127">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="91cc7-127">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91cc7-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="91cc7-128">-Name</span></span>
<span data-ttu-id="91cc7-129">Określa nazwę maszyny wirtualnej, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91cc7-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91cc7-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="91cc7-130">-NoWait</span></span>
<span data-ttu-id="91cc7-131">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="91cc7-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="91cc7-132">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="91cc7-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91cc7-133">— Ponowne aplikacji</span><span class="sxs-lookup"><span data-stu-id="91cc7-133">-Reapply</span></span>
<span data-ttu-id="91cc7-134">Aby ponownie aplikacji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="91cc7-134">To reapply virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReapplyResourceGroupNameParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91cc7-135">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="91cc7-135">-Redeploy</span></span>
<span data-ttu-id="91cc7-136">Wskazuje, że to polecenie cmdlet ręcznie ponownie przekieruje maszynę wirtualną do innego hosta platformy Azure w celu rozwiązania problemów.</span><span class="sxs-lookup"><span data-stu-id="91cc7-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="91cc7-137">Ponowne uruchomienie maszyny wirtualnej powoduje jej utratę danych na dysku.</span><span class="sxs-lookup"><span data-stu-id="91cc7-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91cc7-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91cc7-138">-ResourceGroupName</span></span>
<span data-ttu-id="91cc7-139">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="91cc7-139">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91cc7-140">—SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="91cc7-140">-SimulateEviction</span></span>
<span data-ttu-id="91cc7-141">Wskazuje, że to polecenie cmdlet symuluje wywłaszanie maszyny wirtualnej na miejscu.</span><span class="sxs-lookup"><span data-stu-id="91cc7-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="91cc7-142">Wywłaszczenie nastąpi w ciągu 30 minut od wywołania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="91cc7-142">The eviction will occur within 30 minutes of calling the API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimulateEvictionResourceGroupNameParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91cc7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91cc7-143">CommonParameters</span></span>
<span data-ttu-id="91cc7-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91cc7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91cc7-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91cc7-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91cc7-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91cc7-146">INPUTS</span></span>

### <span data-ttu-id="91cc7-147">System.String</span><span class="sxs-lookup"><span data-stu-id="91cc7-147">System.String</span></span>

## <span data-ttu-id="91cc7-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91cc7-148">OUTPUTS</span></span>

### <span data-ttu-id="91cc7-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="91cc7-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="91cc7-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="91cc7-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="91cc7-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="91cc7-151">NOTES</span></span>

## <span data-ttu-id="91cc7-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91cc7-152">RELATED LINKS</span></span>

[<span data-ttu-id="91cc7-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="91cc7-153">Get-AzVM</span></span>](./Get-AzVM.md)


