---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: c1280b6e59b4dc1c4ddd70b924863eacce0c6e81
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893493"
---
# <span data-ttu-id="bfe2c-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bfe2c-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="bfe2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bfe2c-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe2c-103">Usuwa rozszerzenie diagnostyczne z VMSS.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="bfe2c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bfe2c-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfe2c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bfe2c-105">DESCRIPTION</span></span>
<span data-ttu-id="bfe2c-106">Polecenie cmdlet **Remove-AzVmssDiagnosticsExtension** usuwa rozszerzenie diagnostyczne z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="bfe2c-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="bfe2c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bfe2c-107">EXAMPLES</span></span>

### <span data-ttu-id="bfe2c-108">Przykład 1: Usuwanie rozszerzenia diagnostycznego z VMSS</span><span class="sxs-lookup"><span data-stu-id="bfe2c-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="bfe2c-109">To polecenie usuwa rozszerzenie diagnostyczne z VMSS.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="bfe2c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bfe2c-110">PARAMETERS</span></span>

### <span data-ttu-id="bfe2c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfe2c-111">-DefaultProfile</span></span>
<span data-ttu-id="bfe2c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfe2c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bfe2c-113">-Name</span></span>
<span data-ttu-id="bfe2c-114">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="bfe2c-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bfe2c-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bfe2c-116">Określa VMSS, z którego należy usunąć rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="bfe2c-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bfe2c-117">-Confirm</span></span>
<span data-ttu-id="bfe2c-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfe2c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfe2c-119">-WhatIf</span></span>
<span data-ttu-id="bfe2c-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="bfe2c-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfe2c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe2c-122">CommonParameters</span></span>
<span data-ttu-id="bfe2c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe2c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfe2c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe2c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfe2c-125">INPUTS</span></span>

### <span data-ttu-id="bfe2c-126">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bfe2c-126">VirtualMachineScaleSet</span></span>
<span data-ttu-id="bfe2c-127">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="bfe2c-127">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="bfe2c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bfe2c-128">OUTPUTS</span></span>

###  
<span data-ttu-id="bfe2c-129">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="bfe2c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bfe2c-130">NOTES</span></span>

## <span data-ttu-id="bfe2c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfe2c-131">RELATED LINKS</span></span>

[<span data-ttu-id="bfe2c-132">Dodaj-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bfe2c-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="bfe2c-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bfe2c-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="bfe2c-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="bfe2c-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


