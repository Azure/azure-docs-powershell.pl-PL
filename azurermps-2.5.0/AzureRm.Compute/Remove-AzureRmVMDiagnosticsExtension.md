---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 57e3aef7ff5b6acece0ccba1505d33f2add05ae2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898793"
---
# <span data-ttu-id="bb72a-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bb72a-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="bb72a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb72a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb72a-103">Usuwa rozszerzenie diagnostyki z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bb72a-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb72a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb72a-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb72a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb72a-105">DESCRIPTION</span></span>
<span data-ttu-id="bb72a-106">Polecenie cmdlet **Remove-AzureRmVMDiagnosticsExtension** usuwa rozszerzenie Diagnostyka platformy Azure z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bb72a-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="bb72a-107">Musisz przekazać dane wyjściowe tego polecenia cmdlet do polecenia cmdlet Update-AzureRmVM, aby zaimplementować wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="bb72a-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="bb72a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb72a-108">EXAMPLES</span></span>

### <span data-ttu-id="bb72a-109">Przykład 1: Usuwanie rozszerzenia diagnostycznego z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="bb72a-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="bb72a-110">To polecenie usuwa rozszerzenie diagnostyczne z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="bb72a-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="bb72a-111">Polecenie przekazuje wynik do polecenia cmdlet Update-AzureRmVM przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="bb72a-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bb72a-112">To polecenie aktualizuje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="bb72a-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="bb72a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb72a-113">PARAMETERS</span></span>

### <span data-ttu-id="bb72a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb72a-114">-DefaultProfile</span></span>
<span data-ttu-id="bb72a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb72a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb72a-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bb72a-116">-Name</span></span>
<span data-ttu-id="bb72a-117">Określa nazwę rozszerzenia diagnostycznego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb72a-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bb72a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb72a-118">-ResourceGroupName</span></span>
<span data-ttu-id="bb72a-119">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bb72a-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bb72a-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="bb72a-120">-VMName</span></span>
<span data-ttu-id="bb72a-121">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="bb72a-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="bb72a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb72a-122">CommonParameters</span></span>
<span data-ttu-id="bb72a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb72a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb72a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb72a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb72a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb72a-125">INPUTS</span></span>

### <span data-ttu-id="bb72a-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bb72a-126">None</span></span>
<span data-ttu-id="bb72a-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="bb72a-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb72a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb72a-128">OUTPUTS</span></span>

### <span data-ttu-id="bb72a-129">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bb72a-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bb72a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb72a-130">NOTES</span></span>

## <span data-ttu-id="bb72a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb72a-131">RELATED LINKS</span></span>

[<span data-ttu-id="bb72a-132">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bb72a-132">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="bb72a-133">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bb72a-133">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="bb72a-134">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bb72a-134">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


