---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 89ab4ea57f5f03fbc26d33e1a9087371f215d4ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525302"
---
# <span data-ttu-id="f0ab5-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f0ab5-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="f0ab5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ab5-103">Usuwa interfejs sieciowy z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0ab5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0ab5-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0ab5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f0ab5-105">DESCRIPTION</span></span>
<span data-ttu-id="f0ab5-106">Polecenie cmdlet **Remove-AzureRmVMNetworkInterface** Usuwa interfejs sieciowy z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="f0ab5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0ab5-107">EXAMPLES</span></span>

## <span data-ttu-id="f0ab5-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0ab5-108">PARAMETERS</span></span>

### <span data-ttu-id="f0ab5-109">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="f0ab5-109">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="f0ab5-110">Określa tablicę identyfikatorów interfejsów sieciowych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-110">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ab5-111">-VM</span><span class="sxs-lookup"><span data-stu-id="f0ab5-111">-VM</span></span>
<span data-ttu-id="f0ab5-112">Umożliwia określenie maszyny wirtualnej, z poziomu której to polecenie cmdlet Usuwa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-112">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="f0ab5-113">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-113">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ab5-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0ab5-114">-Confirm</span></span>
<span data-ttu-id="f0ab5-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-115">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="f0ab5-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ab5-116">-WhatIf</span></span>
<span data-ttu-id="f0ab5-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0ab5-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-118">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="f0ab5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ab5-119">CommonParameters</span></span>
<span data-ttu-id="f0ab5-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ab5-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0ab5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ab5-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0ab5-122">INPUTS</span></span>

### <span data-ttu-id="f0ab5-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f0ab5-123">None</span></span>
<span data-ttu-id="f0ab5-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0ab5-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0ab5-125">OUTPUTS</span></span>

## <span data-ttu-id="f0ab5-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0ab5-126">NOTES</span></span>

## <span data-ttu-id="f0ab5-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0ab5-127">RELATED LINKS</span></span>

[<span data-ttu-id="f0ab5-128">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f0ab5-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


