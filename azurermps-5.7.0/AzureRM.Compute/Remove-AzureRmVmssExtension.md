---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 09b90d5ef1f3852f7da39efac9167a8329fba85f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544448"
---
# <span data-ttu-id="8f0db-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8f0db-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="8f0db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f0db-102">SYNOPSIS</span></span>
<span data-ttu-id="8f0db-103">Usuwa rozszerzenie z VMSS.</span><span class="sxs-lookup"><span data-stu-id="8f0db-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f0db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f0db-104">SYNTAX</span></span>

### <span data-ttu-id="8f0db-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f0db-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f0db-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f0db-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Id] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f0db-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8f0db-107">DESCRIPTION</span></span>
<span data-ttu-id="8f0db-108">Polecenie cmdlet **Remove-AzureRmVmssExtension** usuwa rozszerzenie z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8f0db-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8f0db-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f0db-109">EXAMPLES</span></span>

## <span data-ttu-id="8f0db-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f0db-110">PARAMETERS</span></span>

### <span data-ttu-id="8f0db-111">-ID</span><span class="sxs-lookup"><span data-stu-id="8f0db-111">-Id</span></span>
<span data-ttu-id="8f0db-112">Określa identyfikator rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="8f0db-112">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f0db-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8f0db-113">-Name</span></span>
<span data-ttu-id="8f0db-114">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="8f0db-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f0db-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8f0db-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8f0db-116">Określa VMSS, z którego ma zostać usunięte rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="8f0db-116">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="8f0db-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f0db-117">-Confirm</span></span>
<span data-ttu-id="8f0db-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f0db-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0db-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f0db-119">-WhatIf</span></span>
<span data-ttu-id="8f0db-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f0db-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f0db-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8f0db-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0db-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f0db-122">CommonParameters</span></span>
<span data-ttu-id="8f0db-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f0db-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f0db-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f0db-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f0db-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f0db-125">INPUTS</span></span>

### <span data-ttu-id="8f0db-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8f0db-126">None</span></span>
<span data-ttu-id="8f0db-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8f0db-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f0db-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f0db-128">OUTPUTS</span></span>

### <span data-ttu-id="8f0db-129">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8f0db-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8f0db-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f0db-130">NOTES</span></span>

## <span data-ttu-id="8f0db-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f0db-131">RELATED LINKS</span></span>

[<span data-ttu-id="8f0db-132">Dodaj-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8f0db-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
