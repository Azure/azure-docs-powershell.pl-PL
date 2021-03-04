---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: efe587cf01fa2adf16e4b6beaaa319312f3c9fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969569"
---
# <span data-ttu-id="31dda-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="31dda-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="31dda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31dda-102">SYNOPSIS</span></span>
<span data-ttu-id="31dda-103">Dodaje interfejs sieciowy do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="31dda-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="31dda-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="31dda-104">SYNTAX</span></span>

### <span data-ttu-id="31dda-105">GetNicFromNicId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="31dda-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31dda-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="31dda-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31dda-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="31dda-107">DESCRIPTION</span></span>
<span data-ttu-id="31dda-108">Polecenie **cmdlet Add-AzVMNetworkInterface** dodaje interfejs sieciowy do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="31dda-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="31dda-109">Interfejs można dodać podczas tworzenia maszyny wirtualnej lub do istniejącej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="31dda-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="31dda-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="31dda-110">EXAMPLES</span></span>

### <span data-ttu-id="31dda-111">Przykład 1. Dodawanie interfejsu sieciowego do nowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="31dda-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="31dda-112">Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="31dda-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="31dda-113">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="31dda-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="31dda-114">Drugie polecenie dodaje interfejs sieciowy do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="31dda-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="31dda-115">Przykład 2. Dodawanie interfejsu sieciowego do istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="31dda-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="31dda-116">Pierwsze polecenie pobiera maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="31dda-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="31dda-117">Polecenie przechowuje maszynę wirtualną w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="31dda-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="31dda-118">Drugie polecenie dodaje interfejs sieciowy do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="31dda-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="31dda-119">Ostatnie polecenie aktualizuje stan maszyny wirtualnej przechowywanej w u $VirtualMachine ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="31dda-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="31dda-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31dda-120">PARAMETERS</span></span>

### <span data-ttu-id="31dda-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31dda-121">-DefaultProfile</span></span>
<span data-ttu-id="31dda-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="31dda-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31dda-123">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="31dda-123">-Id</span></span>
<span data-ttu-id="31dda-124">Określa identyfikator interfejsu sieciowego do dodania do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="31dda-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="31dda-125">Aby uzyskać interfejs sieciowy, możesz użyć polecenia cmdlet [Get-AzNetworkInterface.](/powershell/module/az.network/get-aznetworkinterface)</span><span class="sxs-lookup"><span data-stu-id="31dda-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31dda-126">- NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="31dda-126">-NetworkInterface</span></span>
<span data-ttu-id="31dda-127">Określa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="31dda-127">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31dda-128">— podstawowy</span><span class="sxs-lookup"><span data-stu-id="31dda-128">-Primary</span></span>
<span data-ttu-id="31dda-129">Wskazuje, że to polecenie cmdlet dodaje interfejs sieciowy jako interfejs podstawowy.</span><span class="sxs-lookup"><span data-stu-id="31dda-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31dda-130">— MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="31dda-130">-VM</span></span>
<span data-ttu-id="31dda-131">Określa lokalny obiekt maszyny wirtualnej, do którego ma być dodać interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="31dda-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="31dda-132">Aby utworzyć maszynę wirtualną, użyj polecenia cmdlet **New-AzVMConfig.**</span><span class="sxs-lookup"><span data-stu-id="31dda-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="31dda-133">Aby uzyskać istniejącą maszynę wirtualną, użyj polecenia cmdlet **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="31dda-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31dda-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31dda-134">CommonParameters</span></span>
<span data-ttu-id="31dda-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31dda-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31dda-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31dda-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31dda-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31dda-137">INPUTS</span></span>

### <span data-ttu-id="31dda-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="31dda-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="31dda-139">System.String</span><span class="sxs-lookup"><span data-stu-id="31dda-139">System.String</span></span>

### <span data-ttu-id="31dda-140">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="31dda-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="31dda-141">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="31dda-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="31dda-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31dda-142">OUTPUTS</span></span>

### <span data-ttu-id="31dda-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="31dda-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="31dda-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="31dda-144">NOTES</span></span>

## <span data-ttu-id="31dda-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31dda-145">RELATED LINKS</span></span>

[<span data-ttu-id="31dda-146">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="31dda-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="31dda-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="31dda-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="31dda-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="31dda-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
