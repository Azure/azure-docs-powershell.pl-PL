---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: 4d8f3afcddeff0d854ce8d0947e75b155d78a896
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869167"
---
# <span data-ttu-id="204fb-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="204fb-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="204fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="204fb-102">SYNOPSIS</span></span>
<span data-ttu-id="204fb-103">Dodaje interfejs sieciowy do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="204fb-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="204fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="204fb-104">SYNTAX</span></span>

### <span data-ttu-id="204fb-105">GetNicFromNicId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="204fb-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="204fb-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="204fb-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="204fb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="204fb-107">DESCRIPTION</span></span>
<span data-ttu-id="204fb-108">Polecenie cmdlet **Add-AzVMNetworkInterface** umożliwia dodanie interfejsu sieciowego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="204fb-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="204fb-109">Podczas tworzenia maszyny wirtualnej lub dodawania jej do istniejącej maszyny wirtualnej można dodać interfejs.</span><span class="sxs-lookup"><span data-stu-id="204fb-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="204fb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="204fb-110">EXAMPLES</span></span>

### <span data-ttu-id="204fb-111">Przykład 1: Dodawanie interfejsu sieciowego do nowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="204fb-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="204fb-112">Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="204fb-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="204fb-113">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="204fb-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="204fb-114">Drugie polecenie dodaje interfejs sieciowy do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="204fb-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="204fb-115">Przykład 2: Dodawanie interfejsu sieciowego do istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="204fb-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="204fb-116">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="204fb-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="204fb-117">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="204fb-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="204fb-118">Drugie polecenie dodaje interfejs sieciowy do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="204fb-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="204fb-119">Polecenie ostatnie umożliwia zaktualizowanie stanu maszyny wirtualnej przechowywanej w $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="204fb-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="204fb-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="204fb-120">PARAMETERS</span></span>

### <span data-ttu-id="204fb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204fb-121">-DefaultProfile</span></span>
<span data-ttu-id="204fb-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="204fb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="204fb-123">-ID</span><span class="sxs-lookup"><span data-stu-id="204fb-123">-Id</span></span>
<span data-ttu-id="204fb-124">Określa identyfikator interfejsu sieciowego, który ma zostać dodany do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="204fb-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="204fb-125">Aby uzyskać interfejs sieciowy, można użyć polecenia cmdlet [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) .</span><span class="sxs-lookup"><span data-stu-id="204fb-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="204fb-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="204fb-126">-NetworkInterface</span></span>
<span data-ttu-id="204fb-127">Określa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="204fb-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="204fb-128">-Primary</span><span class="sxs-lookup"><span data-stu-id="204fb-128">-Primary</span></span>
<span data-ttu-id="204fb-129">Wskazuje, że to polecenie cmdlet dodaje interfejs sieciowy jako podstawowy interfejs.</span><span class="sxs-lookup"><span data-stu-id="204fb-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="204fb-130">-VM</span><span class="sxs-lookup"><span data-stu-id="204fb-130">-VM</span></span>
<span data-ttu-id="204fb-131">Określa obiekt lokalnego maszyny wirtualnej, do którego ma zostać dodany interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="204fb-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="204fb-132">Aby utworzyć maszynę wirtualną, użyj polecenia cmdlet **New-AzVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="204fb-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="204fb-133">Aby uzyskać istniejącą maszynę wirtualną, użyj polecenia cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="204fb-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

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

### <span data-ttu-id="204fb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204fb-134">CommonParameters</span></span>
<span data-ttu-id="204fb-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="204fb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204fb-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="204fb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204fb-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="204fb-137">INPUTS</span></span>

### <span data-ttu-id="204fb-138">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="204fb-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="204fb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="204fb-139">System.String</span></span>

### <span data-ttu-id="204fb-140">System. Collections. Generic. list "1 [[Microsoft. Azure. Management. Internal. Network. Common. INetworkInterfaceReference, Microsoft. Azure. PowerShell. klienci. Network, wersja = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="204fb-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="204fb-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="204fb-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="204fb-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="204fb-142">OUTPUTS</span></span>

### <span data-ttu-id="204fb-143">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="204fb-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="204fb-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="204fb-144">NOTES</span></span>

## <span data-ttu-id="204fb-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="204fb-145">RELATED LINKS</span></span>

[<span data-ttu-id="204fb-146">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="204fb-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="204fb-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="204fb-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="204fb-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="204fb-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
