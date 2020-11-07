---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsshpublickey
schema: 2.0.0
ms.openlocfilehash: c8109a1fa13bff2a2a527bb7e1f9cb232d0e61c3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899002"
---
# <span data-ttu-id="2bba3-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="2bba3-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="2bba3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2bba3-102">SYNOPSIS</span></span>
<span data-ttu-id="2bba3-103">Dodaje klucze publiczne dla protokołu SSH dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2bba3-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bba3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2bba3-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bba3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2bba3-105">DESCRIPTION</span></span>
<span data-ttu-id="2bba3-106">Polecenie cmdlet **Add-AzureRmVMSshPublicKey** umożliwia dodanie kluczy publicznych, których można używać do nawiązywania połączenia z maszyną wirtualną za pośrednictwem bezpiecznego powłoki (SSH).</span><span class="sxs-lookup"><span data-stu-id="2bba3-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="2bba3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2bba3-107">EXAMPLES</span></span>

### <span data-ttu-id="2bba3-108">Przykład 1: Dodawanie klucza publicznego do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2bba3-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="2bba3-109">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="2bba3-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="2bba3-110">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2bba3-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="2bba3-111">Drugie polecenie dodaje klucz publiczny do lokalizacji na VirtualMachine07, że parametr path określa.</span><span class="sxs-lookup"><span data-stu-id="2bba3-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="2bba3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2bba3-112">PARAMETERS</span></span>

### <span data-ttu-id="2bba3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bba3-113">-DefaultProfile</span></span>
<span data-ttu-id="2bba3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2bba3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bba3-115">-Dane</span><span class="sxs-lookup"><span data-stu-id="2bba3-115">-KeyData</span></span>
<span data-ttu-id="2bba3-116">Określa kodowanie bazowe 64 klucza publicznego.</span><span class="sxs-lookup"><span data-stu-id="2bba3-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="2bba3-117">Możesz połączyć się z maszyną wirtualną przy użyciu protokołu SSH lub przy użyciu klucza określającego ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2bba3-117">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="2bba3-118">-Path</span><span class="sxs-lookup"><span data-stu-id="2bba3-118">-Path</span></span>
<span data-ttu-id="2bba3-119">Określa pełną ścieżkę pliku na maszynie wirtualnej, gdzie to polecenie cmdlet przechowuje klucz publiczny SSH.</span><span class="sxs-lookup"><span data-stu-id="2bba3-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="2bba3-120">Jeśli plik już istnieje, to polecenie cmdlet dołącza klucz do pliku.</span><span class="sxs-lookup"><span data-stu-id="2bba3-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="2bba3-121">-VM</span><span class="sxs-lookup"><span data-stu-id="2bba3-121">-VM</span></span>
<span data-ttu-id="2bba3-122">Określa obiekt maszyny wirtualnej, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bba3-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="2bba3-123">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="2bba3-123">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="2bba3-124">Za pomocą polecenia cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) można utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2bba3-124">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="2bba3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bba3-125">CommonParameters</span></span>
<span data-ttu-id="2bba3-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bba3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bba3-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bba3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bba3-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2bba3-128">INPUTS</span></span>

### <span data-ttu-id="2bba3-129">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2bba3-129">PSVirtualMachine</span></span>
<span data-ttu-id="2bba3-130">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="2bba3-130">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="2bba3-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2bba3-131">OUTPUTS</span></span>

### <span data-ttu-id="2bba3-132">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2bba3-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2bba3-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2bba3-133">NOTES</span></span>

## <span data-ttu-id="2bba3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2bba3-134">RELATED LINKS</span></span>

[<span data-ttu-id="2bba3-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2bba3-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="2bba3-136">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="2bba3-136">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
