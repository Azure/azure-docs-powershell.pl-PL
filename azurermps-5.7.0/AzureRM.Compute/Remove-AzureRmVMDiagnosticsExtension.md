---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: b9c2499c3172fcd34000c8adaa0bde144217bcbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544456"
---
# <span data-ttu-id="72827-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="72827-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="72827-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72827-102">SYNOPSIS</span></span>
<span data-ttu-id="72827-103">Usuwa rozszerzenie diagnostyki z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72827-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72827-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72827-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="72827-105">Opis</span><span class="sxs-lookup"><span data-stu-id="72827-105">DESCRIPTION</span></span>
<span data-ttu-id="72827-106">Polecenie cmdlet **Remove-AzureRmVMDiagnosticsExtension** usuwa rozszerzenie Diagnostyka platformy Azure z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72827-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="72827-107">Musisz przekazać dane wyjściowe tego polecenia cmdlet do polecenia cmdlet Update-AzureRmVM, aby zaimplementować wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="72827-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="72827-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72827-108">EXAMPLES</span></span>

### <span data-ttu-id="72827-109">Przykład 1: Usuwanie rozszerzenia diagnostycznego z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="72827-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="72827-110">To polecenie usuwa rozszerzenie diagnostyczne z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="72827-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="72827-111">Polecenie przekazuje wynik do polecenia cmdlet Update-AzureRmVM przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="72827-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="72827-112">To polecenie aktualizuje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="72827-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="72827-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72827-113">PARAMETERS</span></span>

### <span data-ttu-id="72827-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72827-114">-Name</span></span>
<span data-ttu-id="72827-115">Określa nazwę rozszerzenia diagnostycznego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72827-115">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="72827-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72827-116">-ResourceGroupName</span></span>
<span data-ttu-id="72827-117">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72827-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="72827-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="72827-118">-VMName</span></span>
<span data-ttu-id="72827-119">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="72827-119">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="72827-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72827-120">CommonParameters</span></span>
<span data-ttu-id="72827-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72827-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72827-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72827-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72827-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72827-123">INPUTS</span></span>

### <span data-ttu-id="72827-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="72827-124">None</span></span>
<span data-ttu-id="72827-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="72827-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72827-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72827-126">OUTPUTS</span></span>

## <span data-ttu-id="72827-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72827-127">NOTES</span></span>

## <span data-ttu-id="72827-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72827-128">RELATED LINKS</span></span>

[<span data-ttu-id="72827-129">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="72827-129">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="72827-130">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="72827-130">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="72827-131">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="72827-131">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


