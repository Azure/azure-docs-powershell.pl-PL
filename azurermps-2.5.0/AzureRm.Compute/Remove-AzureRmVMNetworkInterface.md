---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 0c7900d50074e185d26f4fafccd9b63756749fd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898786"
---
# <span data-ttu-id="08e9a-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="08e9a-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="08e9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="08e9a-103">Usuwa interfejs sieciowy z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="08e9a-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08e9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08e9a-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08e9a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="08e9a-105">DESCRIPTION</span></span>
<span data-ttu-id="08e9a-106">Polecenie cmdlet **Remove-AzureRmVMNetworkInterface** Usuwa interfejs sieciowy z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="08e9a-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="08e9a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08e9a-107">EXAMPLES</span></span>

### <span data-ttu-id="08e9a-108">1:1</span><span class="sxs-lookup"><span data-stu-id="08e9a-108">1:</span></span>
```

```

## <span data-ttu-id="08e9a-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08e9a-109">PARAMETERS</span></span>

### <span data-ttu-id="08e9a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e9a-110">-DefaultProfile</span></span>
<span data-ttu-id="08e9a-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08e9a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08e9a-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="08e9a-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="08e9a-113">Określa tablicę identyfikatorów interfejsów sieciowych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08e9a-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="08e9a-114">-VM</span><span class="sxs-lookup"><span data-stu-id="08e9a-114">-VM</span></span>
<span data-ttu-id="08e9a-115">Umożliwia określenie maszyny wirtualnej, z poziomu której to polecenie cmdlet Usuwa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="08e9a-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="08e9a-116">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="08e9a-116">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="08e9a-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08e9a-117">-Confirm</span></span>
<span data-ttu-id="08e9a-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08e9a-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="08e9a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08e9a-119">-WhatIf</span></span>
<span data-ttu-id="08e9a-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08e9a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08e9a-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08e9a-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="08e9a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e9a-122">CommonParameters</span></span>
<span data-ttu-id="08e9a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e9a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e9a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08e9a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e9a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08e9a-125">INPUTS</span></span>

### <span data-ttu-id="08e9a-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="08e9a-126">PSVirtualMachine</span></span>
<span data-ttu-id="08e9a-127">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="08e9a-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="08e9a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08e9a-128">OUTPUTS</span></span>

### <span data-ttu-id="08e9a-129">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="08e9a-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="08e9a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08e9a-130">NOTES</span></span>

## <span data-ttu-id="08e9a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08e9a-131">RELATED LINKS</span></span>

[<span data-ttu-id="08e9a-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="08e9a-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


