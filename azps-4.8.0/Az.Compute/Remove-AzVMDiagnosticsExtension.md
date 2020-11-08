---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062584"
---
# <span data-ttu-id="4524c-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4524c-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="4524c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4524c-102">SYNOPSIS</span></span>
<span data-ttu-id="4524c-103">Usuwa rozszerzenie diagnostyki z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4524c-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="4524c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4524c-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4524c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4524c-105">DESCRIPTION</span></span>
<span data-ttu-id="4524c-106">Polecenie cmdlet **Remove-AzVMDiagnosticsExtension** usuwa rozszerzenie Diagnostyka platformy Azure z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4524c-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="4524c-107">Musisz przekazać dane wyjściowe tego polecenia cmdlet do polecenia cmdlet Update-AzVM, aby zaimplementować wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="4524c-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="4524c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4524c-108">EXAMPLES</span></span>

### <span data-ttu-id="4524c-109">Przykład 1: Usuwanie rozszerzenia diagnostycznego z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4524c-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="4524c-110">To polecenie usuwa rozszerzenie diagnostyczne z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="4524c-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="4524c-111">Polecenie przekazuje wynik do polecenia cmdlet Update-AzVM przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="4524c-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4524c-112">To polecenie aktualizuje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="4524c-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="4524c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4524c-113">PARAMETERS</span></span>

### <span data-ttu-id="4524c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4524c-114">-DefaultProfile</span></span>
<span data-ttu-id="4524c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4524c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4524c-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4524c-116">-Name</span></span>
<span data-ttu-id="4524c-117">Określa nazwę rozszerzenia diagnostycznego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4524c-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4524c-118">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4524c-118">-NoWait</span></span>
<span data-ttu-id="4524c-119">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="4524c-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="4524c-120">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="4524c-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="4524c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4524c-121">-ResourceGroupName</span></span>
<span data-ttu-id="4524c-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4524c-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4524c-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="4524c-123">-VMName</span></span>
<span data-ttu-id="4524c-124">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="4524c-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="4524c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4524c-125">CommonParameters</span></span>
<span data-ttu-id="4524c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4524c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4524c-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4524c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4524c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4524c-128">INPUTS</span></span>

### <span data-ttu-id="4524c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4524c-129">System.String</span></span>

## <span data-ttu-id="4524c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4524c-130">OUTPUTS</span></span>

### <span data-ttu-id="4524c-131">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4524c-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4524c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4524c-132">NOTES</span></span>

## <span data-ttu-id="4524c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4524c-133">RELATED LINKS</span></span>

[<span data-ttu-id="4524c-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4524c-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="4524c-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4524c-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="4524c-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4524c-136">Update-AzVM</span></span>](./Update-AzVM.md)


