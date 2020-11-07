---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 30abfad8ece22505755cf19f2e129a9dfad82b10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706160"
---
# <span data-ttu-id="8a557-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8a557-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="8a557-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a557-102">SYNOPSIS</span></span>
<span data-ttu-id="8a557-103">Ustawia skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.</span><span class="sxs-lookup"><span data-stu-id="8a557-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="8a557-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a557-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a557-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8a557-105">DESCRIPTION</span></span>
<span data-ttu-id="8a557-106">Ustawia skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.</span><span class="sxs-lookup"><span data-stu-id="8a557-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="8a557-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a557-107">EXAMPLES</span></span>

### <span data-ttu-id="8a557-108">Przykład 1: Ustawianie właściwości profilu diagnostyki rozruchu dla VMSS</span><span class="sxs-lookup"><span data-stu-id="8a557-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="8a557-109">To polecenie służy do ustawiania właściwości profilu diagnostyki rozruchu dla VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="8a557-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="8a557-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a557-110">PARAMETERS</span></span>

### <span data-ttu-id="8a557-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a557-111">-DefaultProfile</span></span>
<span data-ttu-id="8a557-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a557-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a557-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="8a557-113">-Enabled</span></span>
<span data-ttu-id="8a557-114">Czy należy włączyć diagnostykę rozruchu na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8a557-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a557-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="8a557-115">-StorageUri</span></span>
<span data-ttu-id="8a557-116">Identyfikator URI konta magazynu, który ma być używany do umieszczania danych wyjściowych konsoli i zrzutu ekranu.</span><span class="sxs-lookup"><span data-stu-id="8a557-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="8a557-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a557-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8a557-118">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="8a557-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="8a557-119">Aby utworzyć obiekt, możesz użyć polecenia cmdlet New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="8a557-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a557-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a557-120">-Confirm</span></span>
<span data-ttu-id="8a557-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a557-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a557-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a557-122">-WhatIf</span></span>
<span data-ttu-id="8a557-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a557-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a557-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8a557-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a557-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a557-125">CommonParameters</span></span>
<span data-ttu-id="8a557-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a557-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a557-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a557-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a557-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a557-128">INPUTS</span></span>

### <span data-ttu-id="8a557-129">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a557-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8a557-130">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8a557-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8a557-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8a557-131">System.String</span></span>

## <span data-ttu-id="8a557-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a557-132">OUTPUTS</span></span>

### <span data-ttu-id="8a557-133">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a557-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8a557-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a557-134">NOTES</span></span>

## <span data-ttu-id="8a557-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a557-135">RELATED LINKS</span></span>