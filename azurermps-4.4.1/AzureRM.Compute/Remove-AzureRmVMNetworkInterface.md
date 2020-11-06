---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: b77d741c0313e202304be3fd51fb3e1cd5b25b94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525642"
---
# <span data-ttu-id="6b6a7-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b6a7-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="6b6a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b6a7-102">SYNOPSIS</span></span>
<span data-ttu-id="6b6a7-103">Usuwa interfejs sieciowy z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6b6a7-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b6a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b6a7-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b6a7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6b6a7-105">DESCRIPTION</span></span>
<span data-ttu-id="6b6a7-106">Polecenie cmdlet **Remove-AzureRmVMNetworkInterface** Usuwa interfejs sieciowy z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6b6a7-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="6b6a7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b6a7-107">EXAMPLES</span></span>

## <span data-ttu-id="6b6a7-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b6a7-108">PARAMETERS</span></span>

### <span data-ttu-id="6b6a7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b6a7-109">-DefaultProfile</span></span>
<span data-ttu-id="6b6a7-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b6a7-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b6a7-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="6b6a7-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="6b6a7-112">Określa tablicę identyfikatorów interfejsów sieciowych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b6a7-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6a7-113">-VM</span><span class="sxs-lookup"><span data-stu-id="6b6a7-113">-VM</span></span>
<span data-ttu-id="6b6a7-114">Umożliwia określenie maszyny wirtualnej, z poziomu której to polecenie cmdlet Usuwa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="6b6a7-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="6b6a7-115">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="6b6a7-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b6a7-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b6a7-116">-Confirm</span></span>
<span data-ttu-id="6b6a7-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b6a7-117">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="6b6a7-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b6a7-118">-WhatIf</span></span>
<span data-ttu-id="6b6a7-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b6a7-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b6a7-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6b6a7-120">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="6b6a7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b6a7-121">CommonParameters</span></span>
<span data-ttu-id="6b6a7-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b6a7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b6a7-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b6a7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b6a7-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b6a7-124">INPUTS</span></span>

## <span data-ttu-id="6b6a7-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b6a7-125">OUTPUTS</span></span>

## <span data-ttu-id="6b6a7-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b6a7-126">NOTES</span></span>

## <span data-ttu-id="6b6a7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b6a7-127">RELATED LINKS</span></span>

[<span data-ttu-id="6b6a7-128">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6b6a7-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


