---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssbootdiagnostic
schema: 2.0.0
ms.openlocfilehash: cca99d994380483465f9026ba8023cd92afc7e37
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897477"
---
# <span data-ttu-id="4c5b0-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4c5b0-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="4c5b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="4c5b0-103">Ustawia skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.</span><span class="sxs-lookup"><span data-stu-id="4c5b0-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c5b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c5b0-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c5b0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4c5b0-105">DESCRIPTION</span></span>
<span data-ttu-id="4c5b0-106">Ustawia skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.</span><span class="sxs-lookup"><span data-stu-id="4c5b0-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="4c5b0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c5b0-107">EXAMPLES</span></span>

### <span data-ttu-id="4c5b0-108">Przykład 1: Ustawianie właściwości profilu diagnostyki rozruchu dla VMSS</span><span class="sxs-lookup"><span data-stu-id="4c5b0-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="4c5b0-109">To polecenie służy do ustawiania właściwości profilu diagnostyki rozruchu dla VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="4c5b0-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="4c5b0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c5b0-110">PARAMETERS</span></span>

### <span data-ttu-id="4c5b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c5b0-111">-DefaultProfile</span></span>
<span data-ttu-id="4c5b0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c5b0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c5b0-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="4c5b0-113">-Enabled</span></span>
<span data-ttu-id="4c5b0-114">Czy należy włączyć diagnostykę rozruchu na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4c5b0-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="4c5b0-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="4c5b0-115">-StorageUri</span></span>
<span data-ttu-id="4c5b0-116">Identyfikator URI konta magazynu, który ma być używany do umieszczania danych wyjściowych konsoli i zrzutu ekranu.</span><span class="sxs-lookup"><span data-stu-id="4c5b0-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="4c5b0-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4c5b0-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4c5b0-118">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="4c5b0-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="4c5b0-119">Aby utworzyć obiekt, możesz użyć polecenia cmdlet New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="4c5b0-119">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="4c5b0-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c5b0-120">-Confirm</span></span>
<span data-ttu-id="4c5b0-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c5b0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c5b0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c5b0-122">-WhatIf</span></span>
<span data-ttu-id="4c5b0-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c5b0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c5b0-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4c5b0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c5b0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c5b0-125">CommonParameters</span></span>
<span data-ttu-id="4c5b0-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c5b0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c5b0-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c5b0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c5b0-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c5b0-128">INPUTS</span></span>

### <span data-ttu-id="4c5b0-129">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4c5b0-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="4c5b0-130">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral; PublicKeyToken = b77a5c561934e089]] system. String</span><span class="sxs-lookup"><span data-stu-id="4c5b0-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="4c5b0-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c5b0-131">OUTPUTS</span></span>

### <span data-ttu-id="4c5b0-132">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4c5b0-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="4c5b0-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c5b0-133">NOTES</span></span>

## <span data-ttu-id="4c5b0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c5b0-134">RELATED LINKS</span></span>

