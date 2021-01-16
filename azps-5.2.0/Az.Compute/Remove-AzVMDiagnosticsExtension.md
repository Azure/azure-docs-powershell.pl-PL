---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330106"
---
# <span data-ttu-id="66203-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="66203-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="66203-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66203-102">SYNOPSIS</span></span>
<span data-ttu-id="66203-103">Usuwa rozszerzenie diagnostyki z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="66203-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="66203-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66203-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66203-105">Opis</span><span class="sxs-lookup"><span data-stu-id="66203-105">DESCRIPTION</span></span>
<span data-ttu-id="66203-106">Polecenie cmdlet **Remove-AzVMDiagnosticsExtension** usuwa rozszerzenie Diagnostyka platformy Azure z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="66203-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="66203-107">Musisz przekazać dane wyjściowe tego polecenia cmdlet do polecenia cmdlet Update-AzVM, aby zaimplementować wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="66203-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="66203-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66203-108">EXAMPLES</span></span>

### <span data-ttu-id="66203-109">Przykład 1: Usuwanie rozszerzenia diagnostycznego z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="66203-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="66203-110">To polecenie usuwa rozszerzenie diagnostyczne z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="66203-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="66203-111">Polecenie przekazuje wynik do polecenia cmdlet Update-AzVM przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="66203-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="66203-112">To polecenie aktualizuje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="66203-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="66203-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66203-113">PARAMETERS</span></span>

### <span data-ttu-id="66203-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66203-114">-DefaultProfile</span></span>
<span data-ttu-id="66203-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66203-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66203-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66203-116">-Name</span></span>
<span data-ttu-id="66203-117">Określa nazwę rozszerzenia diagnostycznego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66203-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="66203-118">-Nowait</span><span class="sxs-lookup"><span data-stu-id="66203-118">-NoWait</span></span>
<span data-ttu-id="66203-119">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="66203-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="66203-120">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="66203-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="66203-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66203-121">-ResourceGroupName</span></span>
<span data-ttu-id="66203-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="66203-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="66203-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="66203-123">-VMName</span></span>
<span data-ttu-id="66203-124">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="66203-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="66203-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66203-125">CommonParameters</span></span>
<span data-ttu-id="66203-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66203-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66203-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66203-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66203-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66203-128">INPUTS</span></span>

### <span data-ttu-id="66203-129">System. String</span><span class="sxs-lookup"><span data-stu-id="66203-129">System.String</span></span>

## <span data-ttu-id="66203-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66203-130">OUTPUTS</span></span>

### <span data-ttu-id="66203-131">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="66203-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="66203-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66203-132">NOTES</span></span>

## <span data-ttu-id="66203-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66203-133">RELATED LINKS</span></span>

[<span data-ttu-id="66203-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="66203-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="66203-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="66203-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="66203-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="66203-136">Update-AzVM</span></span>](./Update-AzVM.md)


