---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: 6931f6d80d3e279259b599b782a505b2a21dd074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553993"
---
# <span data-ttu-id="3fefb-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="3fefb-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="3fefb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3fefb-102">SYNOPSIS</span></span>
<span data-ttu-id="3fefb-103">Konwertuje maszynę wirtualną na dyski oparte na obiektach Blob na maszynę wirtualną z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="3fefb-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fefb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3fefb-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fefb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3fefb-105">DESCRIPTION</span></span>
<span data-ttu-id="3fefb-106">Polecenie cmdlet **ConvertTo-AzureRmVMManagedDisk** umożliwia konwertowanie maszyny wirtualnej z dyskami typu BLOB na maszynę wirtualną z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="3fefb-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="3fefb-107">Przed wywołaniem tej operacji maszyna wirtualna musi zostać zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="3fefb-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="3fefb-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3fefb-108">EXAMPLES</span></span>

### <span data-ttu-id="3fefb-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3fefb-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="3fefb-110">To polecenie konwertuje dyski oparte na obiekcie BLOB na maszynie wirtualnej o nazwie "VM01" w grupie zasobów "ResourceGroup01" na dyski zarządzane.</span><span class="sxs-lookup"><span data-stu-id="3fefb-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="3fefb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3fefb-111">PARAMETERS</span></span>

### <span data-ttu-id="3fefb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fefb-112">-DefaultProfile</span></span>
<span data-ttu-id="3fefb-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3fefb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fefb-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fefb-114">-ResourceGroupName</span></span>
<span data-ttu-id="3fefb-115">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3fefb-115">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fefb-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="3fefb-116">-VMName</span></span>
<span data-ttu-id="3fefb-117">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3fefb-117">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fefb-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3fefb-118">-Confirm</span></span>
<span data-ttu-id="3fefb-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fefb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fefb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fefb-120">-WhatIf</span></span>
<span data-ttu-id="3fefb-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fefb-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fefb-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3fefb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fefb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fefb-123">CommonParameters</span></span>
<span data-ttu-id="3fefb-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fefb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fefb-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fefb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fefb-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fefb-126">INPUTS</span></span>

### <span data-ttu-id="3fefb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3fefb-127">System.String</span></span>

## <span data-ttu-id="3fefb-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3fefb-128">OUTPUTS</span></span>

### <span data-ttu-id="3fefb-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="3fefb-129">System.Object</span></span>

## <span data-ttu-id="3fefb-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3fefb-130">NOTES</span></span>

## <span data-ttu-id="3fefb-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fefb-131">RELATED LINKS</span></span>

