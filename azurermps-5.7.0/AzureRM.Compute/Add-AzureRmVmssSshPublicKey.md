---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
ms.openlocfilehash: 6ca619ba75fcf639e36650dc66d45d2f86ec8375
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718957"
---
# <span data-ttu-id="40419-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="40419-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="40419-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40419-102">SYNOPSIS</span></span>
<span data-ttu-id="40419-103">Dodaje klucze publiczne SSH do VMSS.</span><span class="sxs-lookup"><span data-stu-id="40419-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40419-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40419-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40419-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40419-105">DESCRIPTION</span></span>
<span data-ttu-id="40419-106">Polecenie cmdlet **Add-AzureRmVmssSshPublicKey** umożliwia dodanie kluczy publicznych, których można używać do nawiązywania połączenia z maszynami wirtualnymi zestawu skali maszyny wirtualnej (VMSS) za pomocą bezpiecznego powłoki (SSH).</span><span class="sxs-lookup"><span data-stu-id="40419-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="40419-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40419-107">EXAMPLES</span></span>

### <span data-ttu-id="40419-108">Przykład 1: Dodawanie klucza publicznego SSH do VMSS</span><span class="sxs-lookup"><span data-stu-id="40419-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="40419-109">W tym przykładzie dodano klucz publiczny SSH do VMSS.</span><span class="sxs-lookup"><span data-stu-id="40419-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="40419-110">W pierwszym poleceniu użyto polecenia cmdlet **New-AzureRmVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="40419-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="40419-111">Drugie polecenie dodaje klucz SSH z określonymi danymi klucza i zapisuje klucz w określonej ścieżce na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="40419-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="40419-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40419-112">PARAMETERS</span></span>

### <span data-ttu-id="40419-113">-Dane</span><span class="sxs-lookup"><span data-stu-id="40419-113">-KeyData</span></span>
<span data-ttu-id="40419-114">Określa dane klucza publicznego SSH RSA.</span><span class="sxs-lookup"><span data-stu-id="40419-114">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="40419-115">-Path</span><span class="sxs-lookup"><span data-stu-id="40419-115">-Path</span></span>
<span data-ttu-id="40419-116">Określa pełną ścieżkę pliku na maszynie wirtualnej, gdzie to polecenie cmdlet przechowuje klucz publiczny SSH.</span><span class="sxs-lookup"><span data-stu-id="40419-116">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="40419-117">Jeśli plik już istnieje, to polecenie cmdlet dołącza klucz do pliku.</span><span class="sxs-lookup"><span data-stu-id="40419-117">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="40419-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="40419-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="40419-119">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="40419-119">Specifies the VMSS object.</span></span>
<span data-ttu-id="40419-120">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="40419-120">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40419-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40419-121">-Confirm</span></span>
<span data-ttu-id="40419-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40419-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40419-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40419-123">-WhatIf</span></span>
<span data-ttu-id="40419-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40419-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40419-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="40419-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40419-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40419-126">CommonParameters</span></span>
<span data-ttu-id="40419-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40419-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40419-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40419-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40419-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40419-129">INPUTS</span></span>

### <span data-ttu-id="40419-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="40419-130">None</span></span>
<span data-ttu-id="40419-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="40419-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40419-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40419-132">OUTPUTS</span></span>

###  
<span data-ttu-id="40419-133">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="40419-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="40419-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40419-134">NOTES</span></span>

## <span data-ttu-id="40419-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40419-135">RELATED LINKS</span></span>

[<span data-ttu-id="40419-136">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="40419-136">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
