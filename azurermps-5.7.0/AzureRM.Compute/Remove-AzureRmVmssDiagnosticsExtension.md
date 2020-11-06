---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 07f679c714c7c8f6f65f89681e3c8df0fff133df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544544"
---
# <span data-ttu-id="1360e-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1360e-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="1360e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1360e-102">SYNOPSIS</span></span>
<span data-ttu-id="1360e-103">Usuwa rozszerzenie diagnostyczne z VMSS.</span><span class="sxs-lookup"><span data-stu-id="1360e-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1360e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1360e-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1360e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1360e-105">DESCRIPTION</span></span>
<span data-ttu-id="1360e-106">Polecenie cmdlet **Remove-AzureRmVmssDiagnosticsExtension** usuwa rozszerzenie diagnostyczne z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1360e-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1360e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1360e-107">EXAMPLES</span></span>

### <span data-ttu-id="1360e-108">Przykład 1: Usuwanie rozszerzenia diagnostycznego z VMSS</span><span class="sxs-lookup"><span data-stu-id="1360e-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="1360e-109">To polecenie usuwa rozszerzenie diagnostyczne z VMSS.</span><span class="sxs-lookup"><span data-stu-id="1360e-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="1360e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1360e-110">PARAMETERS</span></span>

### <span data-ttu-id="1360e-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1360e-111">-Name</span></span>
<span data-ttu-id="1360e-112">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="1360e-112">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1360e-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1360e-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1360e-114">Określa VMSS, z którego należy usunąć rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="1360e-114">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="1360e-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1360e-115">-Confirm</span></span>
<span data-ttu-id="1360e-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1360e-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1360e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1360e-117">-WhatIf</span></span>
<span data-ttu-id="1360e-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1360e-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1360e-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1360e-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1360e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1360e-120">CommonParameters</span></span>
<span data-ttu-id="1360e-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1360e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1360e-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1360e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1360e-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1360e-123">INPUTS</span></span>

### <span data-ttu-id="1360e-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1360e-124">None</span></span>
<span data-ttu-id="1360e-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1360e-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1360e-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1360e-126">OUTPUTS</span></span>

###  
<span data-ttu-id="1360e-127">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1360e-127">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1360e-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1360e-128">NOTES</span></span>

## <span data-ttu-id="1360e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1360e-129">RELATED LINKS</span></span>

[<span data-ttu-id="1360e-130">Dodaj-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1360e-130">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="1360e-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1360e-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="1360e-132">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="1360e-132">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


