---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 4f69866d6301bc4efc0c867d35cdc7777e759ed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525633"
---
# <span data-ttu-id="30642-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="30642-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="30642-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30642-102">SYNOPSIS</span></span>
<span data-ttu-id="30642-103">Usuwa rozszerzenie diagnostyczne z VMSS.</span><span class="sxs-lookup"><span data-stu-id="30642-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30642-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30642-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30642-105">Opis</span><span class="sxs-lookup"><span data-stu-id="30642-105">DESCRIPTION</span></span>
<span data-ttu-id="30642-106">Polecenie cmdlet **Remove-AzureRmVmssDiagnosticsExtension** usuwa rozszerzenie diagnostyczne z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="30642-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="30642-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30642-107">EXAMPLES</span></span>

### <span data-ttu-id="30642-108">Przykład 1: Usuwanie rozszerzenia diagnostycznego z VMSS</span><span class="sxs-lookup"><span data-stu-id="30642-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="30642-109">To polecenie usuwa rozszerzenie diagnostyczne z VMSS.</span><span class="sxs-lookup"><span data-stu-id="30642-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="30642-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30642-110">PARAMETERS</span></span>

### <span data-ttu-id="30642-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30642-111">-DefaultProfile</span></span>
<span data-ttu-id="30642-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30642-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30642-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="30642-113">-Name</span></span>
<span data-ttu-id="30642-114">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="30642-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="30642-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="30642-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="30642-116">Określa VMSS, z którego należy usunąć rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="30642-116">Specifies the VMSS from which to remove the extension.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30642-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30642-117">-Confirm</span></span>
<span data-ttu-id="30642-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30642-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30642-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30642-119">-WhatIf</span></span>
<span data-ttu-id="30642-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30642-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="30642-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="30642-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30642-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30642-122">CommonParameters</span></span>
<span data-ttu-id="30642-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30642-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30642-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30642-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30642-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30642-125">INPUTS</span></span>

## <span data-ttu-id="30642-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30642-126">OUTPUTS</span></span>

###  
<span data-ttu-id="30642-127">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="30642-127">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="30642-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30642-128">NOTES</span></span>

## <span data-ttu-id="30642-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30642-129">RELATED LINKS</span></span>

[<span data-ttu-id="30642-130">Dodaj-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="30642-130">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="30642-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="30642-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="30642-132">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="30642-132">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


