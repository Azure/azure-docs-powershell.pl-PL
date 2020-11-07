---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: b4cbc3ba7dd90d2810c4833fe1b74c13541fcb7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716857"
---
# <span data-ttu-id="80cd3-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="80cd3-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="80cd3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="80cd3-103">Dodaje klucze publiczne dla protokołu SSH dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="80cd3-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80cd3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80cd3-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="80cd3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="80cd3-105">DESCRIPTION</span></span>
<span data-ttu-id="80cd3-106">Polecenie cmdlet **Add-AzureRmVMSshPublicKey** umożliwia dodanie kluczy publicznych, których można używać do nawiązywania połączenia z maszyną wirtualną za pośrednictwem bezpiecznego powłoki (SSH).</span><span class="sxs-lookup"><span data-stu-id="80cd3-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="80cd3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80cd3-107">EXAMPLES</span></span>

### <span data-ttu-id="80cd3-108">Przykład 1: Dodawanie klucza publicznego do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="80cd3-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="80cd3-109">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="80cd3-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="80cd3-110">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="80cd3-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="80cd3-111">Drugie polecenie dodaje klucz publiczny do lokalizacji na VirtualMachine07, że parametr path określa.</span><span class="sxs-lookup"><span data-stu-id="80cd3-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="80cd3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80cd3-112">PARAMETERS</span></span>

### <span data-ttu-id="80cd3-113">-Dane</span><span class="sxs-lookup"><span data-stu-id="80cd3-113">-KeyData</span></span>
<span data-ttu-id="80cd3-114">Określa kodowanie bazowe 64 klucza publicznego.</span><span class="sxs-lookup"><span data-stu-id="80cd3-114">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="80cd3-115">Możesz połączyć się z maszyną wirtualną przy użyciu protokołu SSH lub przy użyciu klucza określającego ten parametr.</span><span class="sxs-lookup"><span data-stu-id="80cd3-115">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80cd3-116">-Path</span><span class="sxs-lookup"><span data-stu-id="80cd3-116">-Path</span></span>
<span data-ttu-id="80cd3-117">Określa pełną ścieżkę pliku na maszynie wirtualnej, gdzie to polecenie cmdlet przechowuje klucz publiczny SSH.</span><span class="sxs-lookup"><span data-stu-id="80cd3-117">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="80cd3-118">Jeśli plik już istnieje, to polecenie cmdlet dołącza klucz do pliku.</span><span class="sxs-lookup"><span data-stu-id="80cd3-118">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80cd3-119">-VM</span><span class="sxs-lookup"><span data-stu-id="80cd3-119">-VM</span></span>
<span data-ttu-id="80cd3-120">Określa obiekt maszyny wirtualnej, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80cd3-120">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="80cd3-121">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="80cd3-121">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="80cd3-122">Za pomocą polecenia cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) można utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="80cd3-122">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="80cd3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80cd3-123">CommonParameters</span></span>
<span data-ttu-id="80cd3-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80cd3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80cd3-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80cd3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80cd3-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80cd3-126">INPUTS</span></span>

### <span data-ttu-id="80cd3-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="80cd3-127">None</span></span>
<span data-ttu-id="80cd3-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="80cd3-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="80cd3-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80cd3-129">OUTPUTS</span></span>

## <span data-ttu-id="80cd3-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80cd3-130">NOTES</span></span>

## <span data-ttu-id="80cd3-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80cd3-131">RELATED LINKS</span></span>

[<span data-ttu-id="80cd3-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="80cd3-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="80cd3-133">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="80cd3-133">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
