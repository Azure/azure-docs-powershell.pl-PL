---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177554"
---
# <span data-ttu-id="fab39-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fab39-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="fab39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fab39-102">SYNOPSIS</span></span>
<span data-ttu-id="fab39-103">Usuwa rozszerzenie Diagnostyka z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fab39-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="fab39-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fab39-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fab39-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fab39-105">DESCRIPTION</span></span>
<span data-ttu-id="fab39-106">Polecenie **cmdlet Remove-AzVMDiagnosticsExtension** usuwa z maszyny wirtualnej rozszerzenie Azure Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="fab39-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="fab39-107">Musisz przekazać dane wyjściowe tego polecenia cmdlet do Update-AzVM cmdlet, aby zaimplementować zmiany.</span><span class="sxs-lookup"><span data-stu-id="fab39-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="fab39-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fab39-108">EXAMPLES</span></span>

### <span data-ttu-id="fab39-109">Przykład 1. Usunięcie rozszerzenia Diagnostyka z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="fab39-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="fab39-110">To polecenie usuwa rozszerzenie Diagnostyka z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="fab39-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="fab39-111">Polecenie przekazuje wynik do polecenia cmdlet Update-AzVM za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="fab39-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fab39-112">To polecenie aktualizuje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="fab39-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="fab39-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fab39-113">PARAMETERS</span></span>

### <span data-ttu-id="fab39-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab39-114">-DefaultProfile</span></span>
<span data-ttu-id="fab39-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fab39-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fab39-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fab39-116">-Name</span></span>
<span data-ttu-id="fab39-117">Określa nazwę rozszerzenia Diagnostyka, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fab39-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fab39-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fab39-118">-NoWait</span></span>
<span data-ttu-id="fab39-119">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="fab39-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="fab39-120">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="fab39-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab39-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab39-121">-ResourceGroupName</span></span>
<span data-ttu-id="fab39-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fab39-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fab39-123">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="fab39-123">-VMName</span></span>
<span data-ttu-id="fab39-124">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="fab39-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fab39-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab39-125">CommonParameters</span></span>
<span data-ttu-id="fab39-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab39-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab39-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fab39-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab39-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fab39-128">INPUTS</span></span>

### <span data-ttu-id="fab39-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fab39-129">System.String</span></span>

## <span data-ttu-id="fab39-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fab39-130">OUTPUTS</span></span>

### <span data-ttu-id="fab39-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fab39-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fab39-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fab39-132">NOTES</span></span>

## <span data-ttu-id="fab39-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fab39-133">RELATED LINKS</span></span>

[<span data-ttu-id="fab39-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fab39-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="fab39-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fab39-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="fab39-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="fab39-136">Update-AzVM</span></span>](./Update-AzVM.md)


