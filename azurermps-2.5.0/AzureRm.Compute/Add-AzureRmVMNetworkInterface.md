---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 112403f4cb742c5df39538eb2d8d8fac629d3379
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899004"
---
# <span data-ttu-id="6b3f5-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b3f5-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="6b3f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b3f5-102">SYNOPSIS</span></span>
<span data-ttu-id="6b3f5-103">Dodaje interfejs sieciowy do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b3f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b3f5-104">SYNTAX</span></span>

### <span data-ttu-id="6b3f5-105">GetNicFromNicId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6b3f5-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b3f5-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="6b3f5-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b3f5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6b3f5-107">DESCRIPTION</span></span>
<span data-ttu-id="6b3f5-108">Polecenie cmdlet **Add-AzureRmVMNetworkInterface** umożliwia dodanie interfejsu sieciowego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="6b3f5-109">Podczas tworzenia maszyny wirtualnej lub dodawania jej do istniejącej maszyny wirtualnej można dodać interfejs.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="6b3f5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b3f5-110">EXAMPLES</span></span>

### <span data-ttu-id="6b3f5-111">Przykład 1: Dodawanie interfejsu sieciowego do nowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="6b3f5-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="6b3f5-112">Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6b3f5-113">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="6b3f5-114">Drugie polecenie dodaje interfejs sieciowy do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="6b3f5-115">Przykład 2: Dodawanie interfejsu sieciowego do istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="6b3f5-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="6b3f5-116">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="6b3f5-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="6b3f5-117">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="6b3f5-118">Drugie polecenie dodaje interfejs sieciowy do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="6b3f5-119">Polecenie ostatnie umożliwia zaktualizowanie stanu maszyny wirtualnej przechowywanej w $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="6b3f5-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b3f5-120">PARAMETERS</span></span>

### <span data-ttu-id="6b3f5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b3f5-121">-DefaultProfile</span></span>
<span data-ttu-id="6b3f5-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b3f5-123">-ID</span><span class="sxs-lookup"><span data-stu-id="6b3f5-123">-Id</span></span>
<span data-ttu-id="6b3f5-124">Określa identyfikator interfejsu sieciowego, który ma zostać dodany do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="6b3f5-125">Aby uzyskać interfejs sieciowy, można użyć polecenia cmdlet [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) .</span><span class="sxs-lookup"><span data-stu-id="6b3f5-125">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="6b3f5-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b3f5-126">-NetworkInterface</span></span>
<span data-ttu-id="6b3f5-127">Określa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="6b3f5-128">-Primary</span><span class="sxs-lookup"><span data-stu-id="6b3f5-128">-Primary</span></span>
<span data-ttu-id="6b3f5-129">Wskazuje, że to polecenie cmdlet dodaje interfejs sieciowy jako podstawowy interfejs.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="6b3f5-130">-VM</span><span class="sxs-lookup"><span data-stu-id="6b3f5-130">-VM</span></span>
<span data-ttu-id="6b3f5-131">Określa obiekt lokalnego maszyny wirtualnej, do którego ma zostać dodany interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="6b3f5-132">Aby utworzyć maszynę wirtualną, użyj polecenia cmdlet **New-AzureRmVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="6b3f5-132">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="6b3f5-133">Aby uzyskać istniejącą maszynę wirtualną, użyj polecenia cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="6b3f5-133">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

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

### <span data-ttu-id="6b3f5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b3f5-134">CommonParameters</span></span>
<span data-ttu-id="6b3f5-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b3f5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b3f5-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b3f5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b3f5-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b3f5-137">INPUTS</span></span>

### <span data-ttu-id="6b3f5-138">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. Networks. PSNetworkInterface]</span><span class="sxs-lookup"><span data-stu-id="6b3f5-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]</span></span>
<span data-ttu-id="6b3f5-139">Parametr "NetworkInterface" akceptuje wartość typu "System. Collections. Generic. list" 1 [Microsoft. Azure. Commands. Network. models. PSNetworkInterface] "z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6b3f5-139">Parameter 'NetworkInterface' accepts value of type 'System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]' from the pipeline</span></span>

### <span data-ttu-id="6b3f5-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6b3f5-140">PSVirtualMachine</span></span>
<span data-ttu-id="6b3f5-141">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="6b3f5-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="6b3f5-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b3f5-142">OUTPUTS</span></span>

### <span data-ttu-id="6b3f5-143">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6b3f5-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6b3f5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b3f5-144">NOTES</span></span>

## <span data-ttu-id="6b3f5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b3f5-145">RELATED LINKS</span></span>

[<span data-ttu-id="6b3f5-146">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="6b3f5-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="6b3f5-147">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6b3f5-147">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="6b3f5-148">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6b3f5-148">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
