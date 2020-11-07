---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: aaf1162cdeeb007a680a3e9de325cbd10fadef94
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893898"
---
# <span data-ttu-id="c88b8-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c88b8-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="c88b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c88b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c88b8-103">Dodaje interfejs sieciowy do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c88b8-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="c88b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c88b8-104">SYNTAX</span></span>

### <span data-ttu-id="c88b8-105">GetNicFromNicId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c88b8-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c88b8-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="c88b8-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c88b8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c88b8-107">DESCRIPTION</span></span>
<span data-ttu-id="c88b8-108">Polecenie cmdlet **Add-AzVMNetworkInterface** umożliwia dodanie interfejsu sieciowego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c88b8-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="c88b8-109">Podczas tworzenia maszyny wirtualnej lub dodawania jej do istniejącej maszyny wirtualnej można dodać interfejs.</span><span class="sxs-lookup"><span data-stu-id="c88b8-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="c88b8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c88b8-110">EXAMPLES</span></span>

### <span data-ttu-id="c88b8-111">Przykład 1: Dodawanie interfejsu sieciowego do nowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c88b8-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="c88b8-112">Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c88b8-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c88b8-113">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c88b8-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="c88b8-114">Drugie polecenie dodaje interfejs sieciowy do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c88b8-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="c88b8-115">Przykład 2: Dodawanie interfejsu sieciowego do istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c88b8-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="c88b8-116">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="c88b8-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="c88b8-117">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c88b8-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="c88b8-118">Drugie polecenie dodaje interfejs sieciowy do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c88b8-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="c88b8-119">Polecenie ostatnie umożliwia zaktualizowanie stanu maszyny wirtualnej przechowywanej w $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c88b8-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="c88b8-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c88b8-120">PARAMETERS</span></span>

### <span data-ttu-id="c88b8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c88b8-121">-DefaultProfile</span></span>
<span data-ttu-id="c88b8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c88b8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88b8-123">-ID</span><span class="sxs-lookup"><span data-stu-id="c88b8-123">-Id</span></span>
<span data-ttu-id="c88b8-124">Określa identyfikator interfejsu sieciowego, który ma zostać dodany do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c88b8-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="c88b8-125">Aby uzyskać interfejs sieciowy, można użyć polecenia cmdlet [Get-AzNetworkInterface](/powershell/module/azurerm.network/get-aznetworkinterface) .</span><span class="sxs-lookup"><span data-stu-id="c88b8-125">You can use the [Get-AzNetworkInterface](/powershell/module/azurerm.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88b8-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c88b8-126">-NetworkInterface</span></span>
<span data-ttu-id="c88b8-127">Określa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="c88b8-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="c88b8-128">-Primary</span><span class="sxs-lookup"><span data-stu-id="c88b8-128">-Primary</span></span>
<span data-ttu-id="c88b8-129">Wskazuje, że to polecenie cmdlet dodaje interfejs sieciowy jako podstawowy interfejs.</span><span class="sxs-lookup"><span data-stu-id="c88b8-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88b8-130">-VM</span><span class="sxs-lookup"><span data-stu-id="c88b8-130">-VM</span></span>
<span data-ttu-id="c88b8-131">Określa obiekt lokalnego maszyny wirtualnej, do którego ma zostać dodany interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="c88b8-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="c88b8-132">Aby utworzyć maszynę wirtualną, użyj polecenia cmdlet **New-AzVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="c88b8-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="c88b8-133">Aby uzyskać istniejącą maszynę wirtualną, użyj polecenia cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="c88b8-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c88b8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c88b8-134">CommonParameters</span></span>
<span data-ttu-id="c88b8-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c88b8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c88b8-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c88b8-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c88b8-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c88b8-137">INPUTS</span></span>

### <span data-ttu-id="c88b8-138">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. Networks. PSNetworkInterface]</span><span class="sxs-lookup"><span data-stu-id="c88b8-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]</span></span>
<span data-ttu-id="c88b8-139">Parametr "NetworkInterface" akceptuje wartość typu "System. Collections. Generic. list" 1 [Microsoft. Azure. Commands. Network. models. PSNetworkInterface] "z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c88b8-139">Parameter 'NetworkInterface' accepts value of type 'System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]' from the pipeline</span></span>

### <span data-ttu-id="c88b8-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c88b8-140">PSVirtualMachine</span></span>
<span data-ttu-id="c88b8-141">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="c88b8-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="c88b8-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c88b8-142">OUTPUTS</span></span>

### <span data-ttu-id="c88b8-143">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c88b8-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c88b8-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c88b8-144">NOTES</span></span>

## <span data-ttu-id="c88b8-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c88b8-145">RELATED LINKS</span></span>

[<span data-ttu-id="c88b8-146">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="c88b8-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="c88b8-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c88b8-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="c88b8-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c88b8-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
