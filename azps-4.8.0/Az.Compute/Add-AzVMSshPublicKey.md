---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221544"
---
# <span data-ttu-id="232e8-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="232e8-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="232e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="232e8-102">SYNOPSIS</span></span>
<span data-ttu-id="232e8-103">Dodaje klucze publiczne dla funkcji SSH dla maszyny wirtualnej podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="232e8-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="232e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="232e8-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="232e8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="232e8-105">DESCRIPTION</span></span>
<span data-ttu-id="232e8-106">Polecenie cmdlet **Add-AzVMSshPublicKey** umożliwia dodanie kluczy publicznych, których można używać do nawiązywania połączenia z maszyną wirtualną systemu Linux za pośrednictwem bezpiecznego powłoki (SSH).</span><span class="sxs-lookup"><span data-stu-id="232e8-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="232e8-107">Ta funkcja nie może być używana po utworzeniu maszyny wirtualnej, jeśli spróbujesz użyć tej operacji po utworzeniu maszyny wirtualnej bez aktualizacji — AzVM, wystąpi błąd, jeśli użyjesz polecenia z poleceniem Update-AzVM, polecenie wystąpi błąd.</span><span class="sxs-lookup"><span data-stu-id="232e8-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="232e8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="232e8-108">EXAMPLES</span></span>

### <span data-ttu-id="232e8-109">Przykład 1: Dodawanie klucza publicznego do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="232e8-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="232e8-110">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="232e8-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="232e8-111">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="232e8-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="232e8-112">Drugie polecenie dodaje klucz publiczny do lokalizacji na VirtualMachine07, że parametr path określa.</span><span class="sxs-lookup"><span data-stu-id="232e8-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="232e8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="232e8-113">PARAMETERS</span></span>

### <span data-ttu-id="232e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="232e8-114">-DefaultProfile</span></span>
<span data-ttu-id="232e8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="232e8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="232e8-116">-Dane</span><span class="sxs-lookup"><span data-stu-id="232e8-116">-KeyData</span></span>
<span data-ttu-id="232e8-117">Określa kodowanie bazowe 64 klucza publicznego.</span><span class="sxs-lookup"><span data-stu-id="232e8-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="232e8-118">Możesz połączyć się z maszyną wirtualną systemu Linux przy użyciu protokołu SSH lub przy użyciu klucza określającego ten parametr.</span><span class="sxs-lookup"><span data-stu-id="232e8-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232e8-119">-Path</span><span class="sxs-lookup"><span data-stu-id="232e8-119">-Path</span></span>
<span data-ttu-id="232e8-120">Określa pełną ścieżkę pliku na maszynie wirtualnej, gdzie to polecenie cmdlet przechowuje klucz publiczny SSH.</span><span class="sxs-lookup"><span data-stu-id="232e8-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="232e8-121">Jeśli plik już istnieje, to polecenie cmdlet dołącza klucz do pliku.</span><span class="sxs-lookup"><span data-stu-id="232e8-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232e8-122">-VM</span><span class="sxs-lookup"><span data-stu-id="232e8-122">-VM</span></span>
<span data-ttu-id="232e8-123">Określa obiekt maszyny wirtualnej, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="232e8-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="232e8-124">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="232e8-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="232e8-125">Za pomocą polecenia cmdlet [New-AzVMConfig](./New-AzVMConfig.md) można utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="232e8-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="232e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232e8-126">CommonParameters</span></span>
<span data-ttu-id="232e8-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="232e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="232e8-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="232e8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232e8-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="232e8-129">INPUTS</span></span>

### <span data-ttu-id="232e8-130">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="232e8-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="232e8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="232e8-131">System.String</span></span>

## <span data-ttu-id="232e8-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="232e8-132">OUTPUTS</span></span>

### <span data-ttu-id="232e8-133">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="232e8-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="232e8-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="232e8-134">NOTES</span></span>

## <span data-ttu-id="232e8-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="232e8-135">RELATED LINKS</span></span>

[<span data-ttu-id="232e8-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="232e8-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="232e8-137">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="232e8-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
