---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503970"
---
# <span data-ttu-id="bedd4-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="bedd4-101">Set-AzVM</span></span>

## <span data-ttu-id="bedd4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bedd4-102">SYNOPSIS</span></span>
<span data-ttu-id="bedd4-103">Oznacza maszynę wirtualną jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="bedd4-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="bedd4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bedd4-104">SYNTAX</span></span>

### <span data-ttu-id="bedd4-105">GeneralizeResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bedd4-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bedd4-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bedd4-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bedd4-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bedd4-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bedd4-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bedd4-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bedd4-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bedd4-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bedd4-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bedd4-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bedd4-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bedd4-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bedd4-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bedd4-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bedd4-113">Opis</span><span class="sxs-lookup"><span data-stu-id="bedd4-113">DESCRIPTION</span></span>
<span data-ttu-id="bedd4-114">Polecenie cmdlet **Set-AzVM** oznacza maszynę wirtualną jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="bedd4-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="bedd4-115">Przed uruchomieniem tego polecenia cmdlet Zaloguj się do maszyny wirtualnej i przygotuj dysk twardy za pomocą narzędzia Sysprep.</span><span class="sxs-lookup"><span data-stu-id="bedd4-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="bedd4-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bedd4-116">EXAMPLES</span></span>

### <span data-ttu-id="bedd4-117">Przykład 1. Oznaczanie maszyny wirtualnej jako uogólnionej</span><span class="sxs-lookup"><span data-stu-id="bedd4-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="bedd4-118">To polecenie oznacza maszynę wirtualną o nazwie VirtualMachine07 jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="bedd4-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="bedd4-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bedd4-119">PARAMETERS</span></span>

### <span data-ttu-id="bedd4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bedd4-120">-AsJob</span></span>
<span data-ttu-id="bedd4-121">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="bedd4-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bedd4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bedd4-122">-DefaultProfile</span></span>
<span data-ttu-id="bedd4-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bedd4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bedd4-124">-Uogólniona</span><span class="sxs-lookup"><span data-stu-id="bedd4-124">-Generalized</span></span>
<span data-ttu-id="bedd4-125">Wskazuje, że to polecenie cmdlet oznacza maszynę wirtualną jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="bedd4-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="bedd4-126">-ID</span><span class="sxs-lookup"><span data-stu-id="bedd4-126">-Id</span></span>
<span data-ttu-id="bedd4-127">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bedd4-127">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="bedd4-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bedd4-128">-Name</span></span>
<span data-ttu-id="bedd4-129">Określa nazwę maszyny wirtualnej, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bedd4-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bedd4-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bedd4-130">-NoWait</span></span>
<span data-ttu-id="bedd4-131">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="bedd4-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="bedd4-132">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="bedd4-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="bedd4-133">-Ponownie Zastosuj</span><span class="sxs-lookup"><span data-stu-id="bedd4-133">-Reapply</span></span>
<span data-ttu-id="bedd4-134">Ponowne zastosowanie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bedd4-134">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="bedd4-135">-Deploy</span><span class="sxs-lookup"><span data-stu-id="bedd4-135">-Redeploy</span></span>
<span data-ttu-id="bedd4-136">Wskazuje, że to polecenie cmdlet ręcznie ponownie wdraża maszynę wirtualną na innym hoście platformy Azure, aby rozwiązać wszelkie problemy.</span><span class="sxs-lookup"><span data-stu-id="bedd4-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="bedd4-137">Ponowna instalacja maszyny wirtualnej jest uruchamiana ponownie, co powoduje utratę tymczasowych danych dotyczących dysków.</span><span class="sxs-lookup"><span data-stu-id="bedd4-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="bedd4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bedd4-138">-ResourceGroupName</span></span>
<span data-ttu-id="bedd4-139">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bedd4-139">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bedd4-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="bedd4-140">-SimulateEviction</span></span>
<span data-ttu-id="bedd4-141">Wskazuje, że to polecenie cmdlet symuluje wykluczenie dostosowanej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bedd4-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="bedd4-142">Wykluczenie nastąpi w ciągu 30 minut na zadzwonienie do interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="bedd4-142">The eviction will occur within 30 minutes of calling the API.</span></span>

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

### <span data-ttu-id="bedd4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bedd4-143">CommonParameters</span></span>
<span data-ttu-id="bedd4-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bedd4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bedd4-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bedd4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bedd4-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bedd4-146">INPUTS</span></span>

### <span data-ttu-id="bedd4-147">System. String</span><span class="sxs-lookup"><span data-stu-id="bedd4-147">System.String</span></span>

## <span data-ttu-id="bedd4-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bedd4-148">OUTPUTS</span></span>

### <span data-ttu-id="bedd4-149">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="bedd4-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="bedd4-150">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bedd4-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bedd4-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bedd4-151">NOTES</span></span>

## <span data-ttu-id="bedd4-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bedd4-152">RELATED LINKS</span></span>

[<span data-ttu-id="bedd4-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="bedd4-153">Get-AzVM</span></span>](./Get-AzVM.md)


