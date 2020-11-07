---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: 7e1ad3c052c30744762e4e5ec53bfb09b89a3056
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706483"
---
# <span data-ttu-id="97172-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="97172-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="97172-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97172-102">SYNOPSIS</span></span>
<span data-ttu-id="97172-103">Dodaje klucze publiczne dla protokołu SSH dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97172-103">Adds the public keys for SSH for a virtual machine.</span></span>

## <span data-ttu-id="97172-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97172-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97172-105">Opis</span><span class="sxs-lookup"><span data-stu-id="97172-105">DESCRIPTION</span></span>
<span data-ttu-id="97172-106">Polecenie cmdlet **Add-AzVMSshPublicKey** umożliwia dodanie kluczy publicznych, których można używać do nawiązywania połączenia z maszyną wirtualną systemu Linux za pośrednictwem bezpiecznego powłoki (SSH).</span><span class="sxs-lookup"><span data-stu-id="97172-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="97172-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97172-107">EXAMPLES</span></span>

### <span data-ttu-id="97172-108">Przykład 1: Dodawanie klucza publicznego do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="97172-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="97172-109">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="97172-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="97172-110">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="97172-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="97172-111">Drugie polecenie dodaje klucz publiczny do lokalizacji na VirtualMachine07, że parametr path określa.</span><span class="sxs-lookup"><span data-stu-id="97172-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="97172-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97172-112">PARAMETERS</span></span>

### <span data-ttu-id="97172-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97172-113">-DefaultProfile</span></span>
<span data-ttu-id="97172-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="97172-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97172-115">-Dane</span><span class="sxs-lookup"><span data-stu-id="97172-115">-KeyData</span></span>
<span data-ttu-id="97172-116">Określa kodowanie bazowe 64 klucza publicznego.</span><span class="sxs-lookup"><span data-stu-id="97172-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="97172-117">Możesz połączyć się z maszyną wirtualną systemu Linux przy użyciu protokołu SSH lub przy użyciu klucza określającego ten parametr.</span><span class="sxs-lookup"><span data-stu-id="97172-117">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="97172-118">-Path</span><span class="sxs-lookup"><span data-stu-id="97172-118">-Path</span></span>
<span data-ttu-id="97172-119">Określa pełną ścieżkę pliku na maszynie wirtualnej, gdzie to polecenie cmdlet przechowuje klucz publiczny SSH.</span><span class="sxs-lookup"><span data-stu-id="97172-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="97172-120">Jeśli plik już istnieje, to polecenie cmdlet dołącza klucz do pliku.</span><span class="sxs-lookup"><span data-stu-id="97172-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="97172-121">-VM</span><span class="sxs-lookup"><span data-stu-id="97172-121">-VM</span></span>
<span data-ttu-id="97172-122">Określa obiekt maszyny wirtualnej, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97172-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="97172-123">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="97172-123">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="97172-124">Za pomocą polecenia cmdlet [New-AzVMConfig](./New-AzVMConfig.md) można utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97172-124">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="97172-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97172-125">CommonParameters</span></span>
<span data-ttu-id="97172-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97172-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97172-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97172-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97172-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97172-128">INPUTS</span></span>

### <span data-ttu-id="97172-129">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="97172-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="97172-130">System. String</span><span class="sxs-lookup"><span data-stu-id="97172-130">System.String</span></span>

## <span data-ttu-id="97172-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97172-131">OUTPUTS</span></span>

### <span data-ttu-id="97172-132">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="97172-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="97172-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97172-133">NOTES</span></span>

## <span data-ttu-id="97172-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97172-134">RELATED LINKS</span></span>

[<span data-ttu-id="97172-135">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="97172-135">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="97172-136">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="97172-136">New-AzVMConfig</span></span>](./New-AzVMConfig.md)