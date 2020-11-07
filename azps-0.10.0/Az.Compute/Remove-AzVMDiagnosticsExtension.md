---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bec83334032b3d0e18c017bc24d19d381a765176
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893530"
---
# <span data-ttu-id="3a336-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3a336-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="3a336-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a336-102">SYNOPSIS</span></span>
<span data-ttu-id="3a336-103">Usuwa rozszerzenie diagnostyki z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a336-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="3a336-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a336-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a336-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a336-105">DESCRIPTION</span></span>
<span data-ttu-id="3a336-106">Polecenie cmdlet **Remove-AzVMDiagnosticsExtension** usuwa rozszerzenie Diagnostyka platformy Azure z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a336-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="3a336-107">Musisz przekazać dane wyjściowe tego polecenia cmdlet do polecenia cmdlet Update-AzVM, aby zaimplementować wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="3a336-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="3a336-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a336-108">EXAMPLES</span></span>

### <span data-ttu-id="3a336-109">Przykład 1: Usuwanie rozszerzenia diagnostycznego z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="3a336-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="3a336-110">To polecenie usuwa rozszerzenie diagnostyczne z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="3a336-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="3a336-111">Polecenie przekazuje wynik do polecenia cmdlet Update-AzVM przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="3a336-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3a336-112">To polecenie aktualizuje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="3a336-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="3a336-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a336-113">PARAMETERS</span></span>

### <span data-ttu-id="3a336-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a336-114">-DefaultProfile</span></span>
<span data-ttu-id="3a336-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a336-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a336-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a336-116">-Name</span></span>
<span data-ttu-id="3a336-117">Określa nazwę rozszerzenia diagnostycznego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a336-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a336-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a336-118">-ResourceGroupName</span></span>
<span data-ttu-id="3a336-119">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a336-119">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a336-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="3a336-120">-VMName</span></span>
<span data-ttu-id="3a336-121">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="3a336-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a336-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a336-122">CommonParameters</span></span>
<span data-ttu-id="3a336-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a336-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a336-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a336-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a336-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a336-125">INPUTS</span></span>

### <span data-ttu-id="3a336-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3a336-126">None</span></span>
<span data-ttu-id="3a336-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3a336-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a336-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a336-128">OUTPUTS</span></span>

### <span data-ttu-id="3a336-129">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3a336-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3a336-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a336-130">NOTES</span></span>

## <span data-ttu-id="3a336-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a336-131">RELATED LINKS</span></span>

[<span data-ttu-id="3a336-132">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3a336-132">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="3a336-133">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3a336-133">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="3a336-134">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3a336-134">Update-AzVM</span></span>](./Update-AzVM.md)


