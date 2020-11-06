---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: bbfe3018cdf0560b7c7776217ceda7cfe7b77048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553015"
---
# <span data-ttu-id="6d8ef-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6d8ef-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="6d8ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d8ef-102">SYNOPSIS</span></span>
<span data-ttu-id="6d8ef-103">Konwertuje maszynę wirtualną na dyski oparte na obiektach Blob na maszynę wirtualną z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="6d8ef-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d8ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d8ef-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d8ef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d8ef-105">DESCRIPTION</span></span>
<span data-ttu-id="6d8ef-106">Polecenie cmdlet **ConvertTo-AzureRmVMManagedDisk** umożliwia konwertowanie maszyny wirtualnej z dyskami typu BLOB na maszynę wirtualną z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="6d8ef-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="6d8ef-107">Przed wywołaniem tej operacji maszyna wirtualna musi zostać zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="6d8ef-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="6d8ef-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d8ef-108">EXAMPLES</span></span>

### <span data-ttu-id="6d8ef-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d8ef-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="6d8ef-110">To polecenie konwertuje dyski oparte na obiekcie BLOB na maszynie wirtualnej o nazwie "VM01" w grupie zasobów "ResourceGroup01" na dyski zarządzane.</span><span class="sxs-lookup"><span data-stu-id="6d8ef-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="6d8ef-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d8ef-111">PARAMETERS</span></span>

### <span data-ttu-id="6d8ef-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d8ef-112">-ResourceGroupName</span></span>
<span data-ttu-id="6d8ef-113">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d8ef-113">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d8ef-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="6d8ef-114">-VMName</span></span>
<span data-ttu-id="6d8ef-115">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6d8ef-115">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d8ef-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d8ef-116">-Confirm</span></span>
<span data-ttu-id="6d8ef-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d8ef-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d8ef-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d8ef-118">-WhatIf</span></span>
<span data-ttu-id="6d8ef-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d8ef-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d8ef-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d8ef-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d8ef-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d8ef-121">CommonParameters</span></span>
<span data-ttu-id="6d8ef-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d8ef-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d8ef-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d8ef-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d8ef-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d8ef-124">INPUTS</span></span>

### <span data-ttu-id="6d8ef-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6d8ef-125">System.String</span></span>

## <span data-ttu-id="6d8ef-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d8ef-126">OUTPUTS</span></span>

### <span data-ttu-id="6d8ef-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="6d8ef-127">System.Object</span></span>

## <span data-ttu-id="6d8ef-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d8ef-128">NOTES</span></span>

## <span data-ttu-id="6d8ef-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d8ef-129">RELATED LINKS</span></span>

