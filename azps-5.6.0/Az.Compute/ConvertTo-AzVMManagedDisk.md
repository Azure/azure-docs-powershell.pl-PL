---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: f73569e8e40af5111a738496ba6ad41ff03058f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969450"
---
# <span data-ttu-id="9930b-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="9930b-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="9930b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9930b-102">SYNOPSIS</span></span>
<span data-ttu-id="9930b-103">Konwertuje maszynę wirtualną z dyskami na podstawie obiektów blob na maszynę wirtualną z zarządzanymi dyskami.</span><span class="sxs-lookup"><span data-stu-id="9930b-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="9930b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9930b-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9930b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9930b-105">DESCRIPTION</span></span>
<span data-ttu-id="9930b-106">Polecenie cmdlet **ConvertTo-AzVMManaged Należy** przekonwertować maszynę wirtualną z dyskami na podstawie obiektów blob na maszynę wirtualną z zarządzanymi dyskami.</span><span class="sxs-lookup"><span data-stu-id="9930b-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="9930b-107">Aby można było użyć tej operacji, należy zatrzymać deallocated maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9930b-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="9930b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9930b-108">EXAMPLES</span></span>

### <span data-ttu-id="9930b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9930b-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="9930b-110">To polecenie konwertuje dyskietki maszyny wirtualnej o nazwie "WIRTUALNE01" w grupie zasobów "ResourceGroup01" na zarządzane dyskietki.</span><span class="sxs-lookup"><span data-stu-id="9930b-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="9930b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9930b-111">PARAMETERS</span></span>

### <span data-ttu-id="9930b-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9930b-112">-AsJob</span></span>
<span data-ttu-id="9930b-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9930b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9930b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9930b-114">-DefaultProfile</span></span>
<span data-ttu-id="9930b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9930b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9930b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9930b-116">-ResourceGroupName</span></span>
<span data-ttu-id="9930b-117">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9930b-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9930b-118">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="9930b-118">-VMName</span></span>
<span data-ttu-id="9930b-119">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9930b-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="9930b-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9930b-120">-Confirm</span></span>
<span data-ttu-id="9930b-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9930b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9930b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9930b-122">-WhatIf</span></span>
<span data-ttu-id="9930b-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9930b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9930b-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9930b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9930b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9930b-125">CommonParameters</span></span>
<span data-ttu-id="9930b-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9930b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9930b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9930b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9930b-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9930b-128">INPUTS</span></span>

### <span data-ttu-id="9930b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9930b-129">System.String</span></span>

## <span data-ttu-id="9930b-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9930b-130">OUTPUTS</span></span>

### <span data-ttu-id="9930b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9930b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9930b-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9930b-132">NOTES</span></span>

## <span data-ttu-id="9930b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9930b-133">RELATED LINKS</span></span>
