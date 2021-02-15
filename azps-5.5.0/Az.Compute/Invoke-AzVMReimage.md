---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177707"
---
# <span data-ttu-id="b5c55-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="b5c55-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="b5c55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5c55-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c55-103">Ponownie przeprojektuj maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c55-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="b5c55-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b5c55-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5c55-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b5c55-105">DESCRIPTION</span></span>
<span data-ttu-id="b5c55-106">Polecenie cmdlet **Invoke-AzVMReimage** ponownie projektuje maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c55-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="b5c55-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b5c55-107">EXAMPLES</span></span>

### <span data-ttu-id="b5c55-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b5c55-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b5c55-109">To polecenie ponownie dodaje maszynę wirtualną o nazwie VirtualMachine07 w grupie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b5c55-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="b5c55-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5c55-110">PARAMETERS</span></span>

### <span data-ttu-id="b5c55-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b5c55-111">-AsJob</span></span>
<span data-ttu-id="b5c55-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b5c55-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5c55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c55-113">-DefaultProfile</span></span>
<span data-ttu-id="b5c55-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c55-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5c55-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c55-115">-ResourceGroupName</span></span>
<span data-ttu-id="b5c55-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b5c55-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b5c55-117">-Temp Należy</span><span class="sxs-lookup"><span data-stu-id="b5c55-117">-TempDisk</span></span>
<span data-ttu-id="b5c55-118">Określa, czy ponownie zaimportować dysk tymczasowy.</span><span class="sxs-lookup"><span data-stu-id="b5c55-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="b5c55-119">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="b5c55-119">-VMName</span></span>
<span data-ttu-id="b5c55-120">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b5c55-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="b5c55-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5c55-121">-Confirm</span></span>
<span data-ttu-id="b5c55-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b5c55-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5c55-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5c55-123">-WhatIf</span></span>
<span data-ttu-id="b5c55-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5c55-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5c55-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b5c55-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5c55-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c55-126">CommonParameters</span></span>
<span data-ttu-id="b5c55-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c55-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c55-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5c55-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c55-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5c55-129">INPUTS</span></span>

### <span data-ttu-id="b5c55-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b5c55-130">System.String</span></span>

## <span data-ttu-id="b5c55-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5c55-131">OUTPUTS</span></span>

### <span data-ttu-id="b5c55-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b5c55-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b5c55-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b5c55-133">NOTES</span></span>

## <span data-ttu-id="b5c55-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5c55-134">RELATED LINKS</span></span>
