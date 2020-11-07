---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 2fb8d5956cf783940e32f49019115dd911050749
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893861"
---
# <span data-ttu-id="3cacb-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="3cacb-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="3cacb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cacb-102">SYNOPSIS</span></span>
<span data-ttu-id="3cacb-103">Dodaje klucze publiczne SSH do VMSS.</span><span class="sxs-lookup"><span data-stu-id="3cacb-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="3cacb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cacb-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cacb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3cacb-105">DESCRIPTION</span></span>
<span data-ttu-id="3cacb-106">Polecenie cmdlet **Add-AzVmssSshPublicKey** umożliwia dodanie kluczy publicznych, których można używać do nawiązywania połączenia z maszynami wirtualnymi zestawu skali maszyny wirtualnej (VMSS) za pomocą bezpiecznego powłoki (SSH).</span><span class="sxs-lookup"><span data-stu-id="3cacb-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="3cacb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cacb-107">EXAMPLES</span></span>

### <span data-ttu-id="3cacb-108">Przykład 1: Dodawanie klucza publicznego SSH do VMSS</span><span class="sxs-lookup"><span data-stu-id="3cacb-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="3cacb-109">W tym przykładzie dodano klucz publiczny SSH do VMSS.</span><span class="sxs-lookup"><span data-stu-id="3cacb-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="3cacb-110">W pierwszym poleceniu użyto polecenia cmdlet **New-AzVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="3cacb-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="3cacb-111">Drugie polecenie dodaje klucz SSH z określonymi danymi klucza i zapisuje klucz w określonej ścieżce na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3cacb-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="3cacb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cacb-112">PARAMETERS</span></span>

### <span data-ttu-id="3cacb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cacb-113">-DefaultProfile</span></span>
<span data-ttu-id="3cacb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3cacb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cacb-115">-Dane</span><span class="sxs-lookup"><span data-stu-id="3cacb-115">-KeyData</span></span>
<span data-ttu-id="3cacb-116">Określa dane klucza publicznego SSH RSA.</span><span class="sxs-lookup"><span data-stu-id="3cacb-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="3cacb-117">-Path</span><span class="sxs-lookup"><span data-stu-id="3cacb-117">-Path</span></span>
<span data-ttu-id="3cacb-118">Określa pełną ścieżkę pliku na maszynie wirtualnej, gdzie to polecenie cmdlet przechowuje klucz publiczny SSH.</span><span class="sxs-lookup"><span data-stu-id="3cacb-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="3cacb-119">Jeśli plik już istnieje, to polecenie cmdlet dołącza klucz do pliku.</span><span class="sxs-lookup"><span data-stu-id="3cacb-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="3cacb-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3cacb-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3cacb-121">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="3cacb-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="3cacb-122">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="3cacb-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cacb-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3cacb-123">-Confirm</span></span>
<span data-ttu-id="3cacb-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cacb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cacb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cacb-125">-WhatIf</span></span>
<span data-ttu-id="3cacb-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cacb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cacb-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3cacb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cacb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cacb-128">CommonParameters</span></span>
<span data-ttu-id="3cacb-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cacb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cacb-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cacb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cacb-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cacb-131">INPUTS</span></span>

### <span data-ttu-id="3cacb-132">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3cacb-132">VirtualMachineScaleSet</span></span>
<span data-ttu-id="3cacb-133">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="3cacb-133">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="3cacb-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cacb-134">OUTPUTS</span></span>

###  
<span data-ttu-id="3cacb-135">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3cacb-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3cacb-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cacb-136">NOTES</span></span>

## <span data-ttu-id="3cacb-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cacb-137">RELATED LINKS</span></span>

[<span data-ttu-id="3cacb-138">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3cacb-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
