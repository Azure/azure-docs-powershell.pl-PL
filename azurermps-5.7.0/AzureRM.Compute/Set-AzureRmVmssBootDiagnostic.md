---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: 868bf95ca2f54105143f122665ffa89732ada167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546851"
---
# <span data-ttu-id="bc6bb-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bc6bb-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="bc6bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc6bb-102">SYNOPSIS</span></span>
<span data-ttu-id="bc6bb-103">Ustawia skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.</span><span class="sxs-lookup"><span data-stu-id="bc6bb-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc6bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc6bb-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc6bb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bc6bb-105">DESCRIPTION</span></span>
<span data-ttu-id="bc6bb-106">Ustawia skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.</span><span class="sxs-lookup"><span data-stu-id="bc6bb-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="bc6bb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc6bb-107">EXAMPLES</span></span>

### <span data-ttu-id="bc6bb-108">Przykład 1: Ustawianie właściwości profilu diagnostyki rozruchu dla VMSS</span><span class="sxs-lookup"><span data-stu-id="bc6bb-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="bc6bb-109">To polecenie służy do ustawiania właściwości profilu diagnostyki rozruchu dla VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="bc6bb-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="bc6bb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc6bb-110">PARAMETERS</span></span>

### <span data-ttu-id="bc6bb-111">-Enabled</span><span class="sxs-lookup"><span data-stu-id="bc6bb-111">-Enabled</span></span>
<span data-ttu-id="bc6bb-112">Czy należy włączyć diagnostykę rozruchu na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bc6bb-112">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc6bb-113">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="bc6bb-113">-StorageUri</span></span>
<span data-ttu-id="bc6bb-114">Identyfikator URI konta magazynu, który ma być używany do umieszczania danych wyjściowych konsoli i zrzutu ekranu.</span><span class="sxs-lookup"><span data-stu-id="bc6bb-114">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="bc6bb-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bc6bb-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bc6bb-116">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="bc6bb-116">Specifies the VMSS object.</span></span>
<span data-ttu-id="bc6bb-117">Aby utworzyć obiekt, możesz użyć polecenia cmdlet New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="bc6bb-117">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="bc6bb-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc6bb-118">-Confirm</span></span>
<span data-ttu-id="bc6bb-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc6bb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc6bb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc6bb-120">-WhatIf</span></span>
<span data-ttu-id="bc6bb-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc6bb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc6bb-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bc6bb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc6bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc6bb-123">CommonParameters</span></span>
<span data-ttu-id="bc6bb-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc6bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc6bb-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc6bb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc6bb-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc6bb-126">INPUTS</span></span>

### <span data-ttu-id="bc6bb-127">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bc6bb-127">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="bc6bb-128">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral; PublicKeyToken = b77a5c561934e089]] system. String</span><span class="sxs-lookup"><span data-stu-id="bc6bb-128">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="bc6bb-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc6bb-129">OUTPUTS</span></span>

### <span data-ttu-id="bc6bb-130">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bc6bb-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="bc6bb-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc6bb-131">NOTES</span></span>

## <span data-ttu-id="bc6bb-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc6bb-132">RELATED LINKS</span></span>

