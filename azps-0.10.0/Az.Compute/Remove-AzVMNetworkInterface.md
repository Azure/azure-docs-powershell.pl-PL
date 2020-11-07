---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 548d576ff959dd96a6978675ca5a35c18c97e0a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893517"
---
# <span data-ttu-id="ac321-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ac321-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="ac321-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac321-102">SYNOPSIS</span></span>
<span data-ttu-id="ac321-103">Usuwa interfejs sieciowy z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ac321-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="ac321-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac321-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac321-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ac321-105">DESCRIPTION</span></span>
<span data-ttu-id="ac321-106">Polecenie cmdlet **Remove-AzVMNetworkInterface** Usuwa interfejs sieciowy z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ac321-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="ac321-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac321-107">EXAMPLES</span></span>

### <span data-ttu-id="ac321-108">1:1</span><span class="sxs-lookup"><span data-stu-id="ac321-108">1:</span></span>
```

```

## <span data-ttu-id="ac321-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac321-109">PARAMETERS</span></span>

### <span data-ttu-id="ac321-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac321-110">-DefaultProfile</span></span>
<span data-ttu-id="ac321-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac321-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac321-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="ac321-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="ac321-113">Określa tablicę identyfikatorów interfejsów sieciowych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac321-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ac321-114">-VM</span><span class="sxs-lookup"><span data-stu-id="ac321-114">-VM</span></span>
<span data-ttu-id="ac321-115">Umożliwia określenie maszyny wirtualnej, z poziomu której to polecenie cmdlet Usuwa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="ac321-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="ac321-116">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ac321-116">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="ac321-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac321-117">-Confirm</span></span>
<span data-ttu-id="ac321-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac321-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="ac321-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac321-119">-WhatIf</span></span>
<span data-ttu-id="ac321-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac321-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac321-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ac321-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="ac321-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac321-122">CommonParameters</span></span>
<span data-ttu-id="ac321-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac321-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac321-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac321-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac321-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac321-125">INPUTS</span></span>

### <span data-ttu-id="ac321-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ac321-126">PSVirtualMachine</span></span>
<span data-ttu-id="ac321-127">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="ac321-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="ac321-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac321-128">OUTPUTS</span></span>

### <span data-ttu-id="ac321-129">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ac321-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ac321-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac321-130">NOTES</span></span>

## <span data-ttu-id="ac321-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac321-131">RELATED LINKS</span></span>

[<span data-ttu-id="ac321-132">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ac321-132">Get-AzVM</span></span>](./Get-AzVM.md)


