---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199339"
---
# <span data-ttu-id="170b8-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="170b8-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="170b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="170b8-102">SYNOPSIS</span></span>
<span data-ttu-id="170b8-103">Konwertuje maszynę wirtualną z dyskami na podstawie obiektów blob na maszynę wirtualną z zarządzanymi dyskami.</span><span class="sxs-lookup"><span data-stu-id="170b8-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="170b8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="170b8-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="170b8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="170b8-105">DESCRIPTION</span></span>
<span data-ttu-id="170b8-106">Polecenie cmdlet **ConvertTo-AzVMManaged Należy** przekonwertować maszynę wirtualną z dyskami na podstawie obiektów blob na maszynę wirtualną z zarządzanymi dyskami.</span><span class="sxs-lookup"><span data-stu-id="170b8-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="170b8-107">Aby można było użyć tej operacji, należy zatrzymać deallocated maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="170b8-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="170b8-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="170b8-108">EXAMPLES</span></span>

### <span data-ttu-id="170b8-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="170b8-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="170b8-110">To polecenie konwertuje dyskietki maszyny wirtualnej o nazwie "WIRTUALNE01" w grupie zasobów "ResourceGroup01" na zarządzane dyskietki.</span><span class="sxs-lookup"><span data-stu-id="170b8-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="170b8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="170b8-111">PARAMETERS</span></span>

### <span data-ttu-id="170b8-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="170b8-112">-AsJob</span></span>
<span data-ttu-id="170b8-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="170b8-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="170b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170b8-114">-DefaultProfile</span></span>
<span data-ttu-id="170b8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="170b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="170b8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170b8-116">-ResourceGroupName</span></span>
<span data-ttu-id="170b8-117">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="170b8-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="170b8-118">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="170b8-118">-VMName</span></span>
<span data-ttu-id="170b8-119">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="170b8-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="170b8-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="170b8-120">-Confirm</span></span>
<span data-ttu-id="170b8-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="170b8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="170b8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="170b8-122">-WhatIf</span></span>
<span data-ttu-id="170b8-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="170b8-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="170b8-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="170b8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="170b8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170b8-125">CommonParameters</span></span>
<span data-ttu-id="170b8-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="170b8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170b8-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="170b8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170b8-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="170b8-128">INPUTS</span></span>

### <span data-ttu-id="170b8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="170b8-129">System.String</span></span>

## <span data-ttu-id="170b8-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="170b8-130">OUTPUTS</span></span>

### <span data-ttu-id="170b8-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="170b8-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="170b8-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="170b8-132">NOTES</span></span>

## <span data-ttu-id="170b8-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="170b8-133">RELATED LINKS</span></span>
