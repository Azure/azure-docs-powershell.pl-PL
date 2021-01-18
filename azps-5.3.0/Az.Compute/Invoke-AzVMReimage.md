---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504096"
---
# <span data-ttu-id="a46da-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="a46da-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="a46da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a46da-102">SYNOPSIS</span></span>
<span data-ttu-id="a46da-103">Odobrazowanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a46da-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="a46da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a46da-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a46da-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a46da-105">DESCRIPTION</span></span>
<span data-ttu-id="a46da-106">Polecenie cmdlet **Invoke-AzVMReimage** umożliwia odobrazowanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a46da-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="a46da-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a46da-107">EXAMPLES</span></span>

### <span data-ttu-id="a46da-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a46da-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="a46da-109">To polecenie powoduje odobrazowanie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a46da-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="a46da-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a46da-110">PARAMETERS</span></span>

### <span data-ttu-id="a46da-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a46da-111">-AsJob</span></span>
<span data-ttu-id="a46da-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a46da-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a46da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a46da-113">-DefaultProfile</span></span>
<span data-ttu-id="a46da-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a46da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a46da-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a46da-115">-ResourceGroupName</span></span>
<span data-ttu-id="a46da-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a46da-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a46da-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="a46da-117">-TempDisk</span></span>
<span data-ttu-id="a46da-118">Określa, czy dysk tymczasowy ma zostać przeobrazek.</span><span class="sxs-lookup"><span data-stu-id="a46da-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="a46da-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="a46da-119">-VMName</span></span>
<span data-ttu-id="a46da-120">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a46da-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="a46da-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a46da-121">-Confirm</span></span>
<span data-ttu-id="a46da-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a46da-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a46da-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a46da-123">-WhatIf</span></span>
<span data-ttu-id="a46da-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a46da-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a46da-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a46da-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a46da-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a46da-126">CommonParameters</span></span>
<span data-ttu-id="a46da-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a46da-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a46da-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a46da-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a46da-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a46da-129">INPUTS</span></span>

### <span data-ttu-id="a46da-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a46da-130">System.String</span></span>

## <span data-ttu-id="a46da-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a46da-131">OUTPUTS</span></span>

### <span data-ttu-id="a46da-132">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a46da-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a46da-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a46da-133">NOTES</span></span>

## <span data-ttu-id="a46da-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a46da-134">RELATED LINKS</span></span>
