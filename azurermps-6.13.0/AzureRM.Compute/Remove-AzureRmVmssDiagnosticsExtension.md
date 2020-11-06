---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 52b090f433d3d605c870025d696b2572e6938330
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551340"
---
# <span data-ttu-id="56d35-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="56d35-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="56d35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56d35-102">SYNOPSIS</span></span>
<span data-ttu-id="56d35-103">Usuwa rozszerzenie diagnostyczne z VMSS.</span><span class="sxs-lookup"><span data-stu-id="56d35-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56d35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56d35-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56d35-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56d35-105">DESCRIPTION</span></span>
<span data-ttu-id="56d35-106">Polecenie cmdlet **Remove-AzureRmVmssDiagnosticsExtension** usuwa rozszerzenie diagnostyczne z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="56d35-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="56d35-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56d35-107">EXAMPLES</span></span>

### <span data-ttu-id="56d35-108">Przykład 1: Usuwanie rozszerzenia diagnostycznego z VMSS</span><span class="sxs-lookup"><span data-stu-id="56d35-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="56d35-109">To polecenie usuwa rozszerzenie diagnostyczne z VMSS.</span><span class="sxs-lookup"><span data-stu-id="56d35-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="56d35-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56d35-110">PARAMETERS</span></span>

### <span data-ttu-id="56d35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d35-111">-DefaultProfile</span></span>
<span data-ttu-id="56d35-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56d35-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d35-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56d35-113">-Name</span></span>
<span data-ttu-id="56d35-114">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="56d35-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d35-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="56d35-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="56d35-116">Określa VMSS, z którego należy usunąć rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="56d35-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="56d35-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56d35-117">-Confirm</span></span>
<span data-ttu-id="56d35-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d35-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d35-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d35-119">-WhatIf</span></span>
<span data-ttu-id="56d35-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d35-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56d35-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="56d35-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d35-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d35-122">CommonParameters</span></span>
<span data-ttu-id="56d35-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d35-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d35-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56d35-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d35-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56d35-125">INPUTS</span></span>

### <span data-ttu-id="56d35-126">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="56d35-126">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

### <span data-ttu-id="56d35-127">System. String</span><span class="sxs-lookup"><span data-stu-id="56d35-127">System.String</span></span>

## <span data-ttu-id="56d35-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56d35-128">OUTPUTS</span></span>

### <span data-ttu-id="56d35-129">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="56d35-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="56d35-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56d35-130">NOTES</span></span>

## <span data-ttu-id="56d35-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56d35-131">RELATED LINKS</span></span>

[<span data-ttu-id="56d35-132">Dodaj-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="56d35-132">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="56d35-133">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="56d35-133">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="56d35-134">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="56d35-134">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


