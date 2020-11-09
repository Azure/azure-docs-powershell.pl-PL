---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316728"
---
# <span data-ttu-id="424e3-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="424e3-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="424e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="424e3-102">SYNOPSIS</span></span>
<span data-ttu-id="424e3-103">Konwertuje maszynę wirtualną na dyski oparte na obiektach Blob na maszynę wirtualną z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="424e3-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="424e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="424e3-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="424e3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="424e3-105">DESCRIPTION</span></span>
<span data-ttu-id="424e3-106">Polecenie cmdlet **ConvertTo-AzVMManagedDisk** umożliwia konwertowanie maszyny wirtualnej z dyskami typu BLOB na maszynę wirtualną z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="424e3-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="424e3-107">Przed wywołaniem tej operacji maszyna wirtualna musi zostać zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="424e3-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="424e3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="424e3-108">EXAMPLES</span></span>

### <span data-ttu-id="424e3-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="424e3-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="424e3-110">To polecenie konwertuje dyski oparte na obiekcie BLOB na maszynie wirtualnej o nazwie "VM01" w grupie zasobów "ResourceGroup01" na dyski zarządzane.</span><span class="sxs-lookup"><span data-stu-id="424e3-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="424e3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="424e3-111">PARAMETERS</span></span>

### <span data-ttu-id="424e3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="424e3-112">-AsJob</span></span>
<span data-ttu-id="424e3-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="424e3-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424e3-114">-DefaultProfile</span></span>
<span data-ttu-id="424e3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="424e3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424e3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424e3-116">-ResourceGroupName</span></span>
<span data-ttu-id="424e3-117">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="424e3-117">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424e3-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="424e3-118">-VMName</span></span>
<span data-ttu-id="424e3-119">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="424e3-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424e3-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="424e3-120">-Confirm</span></span>
<span data-ttu-id="424e3-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="424e3-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424e3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="424e3-122">-WhatIf</span></span>
<span data-ttu-id="424e3-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="424e3-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="424e3-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="424e3-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424e3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424e3-125">CommonParameters</span></span>
<span data-ttu-id="424e3-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424e3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424e3-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="424e3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424e3-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="424e3-128">INPUTS</span></span>

### <span data-ttu-id="424e3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="424e3-129">System.String</span></span>

## <span data-ttu-id="424e3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="424e3-130">OUTPUTS</span></span>

### <span data-ttu-id="424e3-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="424e3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="424e3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="424e3-132">NOTES</span></span>

## <span data-ttu-id="424e3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="424e3-133">RELATED LINKS</span></span>
