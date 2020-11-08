---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052639"
---
# <span data-ttu-id="247a3-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="247a3-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="247a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="247a3-102">SYNOPSIS</span></span>
<span data-ttu-id="247a3-103">Usuwa obsługę rozszerzeń DSC z maszyny wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="247a3-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="247a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="247a3-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="247a3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="247a3-105">DESCRIPTION</span></span>
<span data-ttu-id="247a3-106">Polecenie cmdlet **Remove-AzVMDscExtension** usuwa zażądaną obsługę rozszerzeń konfiguracji stanu z maszyny wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="247a3-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="247a3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="247a3-107">EXAMPLES</span></span>

### <span data-ttu-id="247a3-108">Przykład 1: Usuwanie rozszerzenia DSC</span><span class="sxs-lookup"><span data-stu-id="247a3-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="247a3-109">To polecenie usuwa rozszerzenie o nazwie DSC na maszynie wirtualnej o nazwie VM07.</span><span class="sxs-lookup"><span data-stu-id="247a3-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="247a3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="247a3-110">PARAMETERS</span></span>

### <span data-ttu-id="247a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="247a3-111">-DefaultProfile</span></span>
<span data-ttu-id="247a3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="247a3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="247a3-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="247a3-113">-Name</span></span>
<span data-ttu-id="247a3-114">Określa nazwę rozszerzenia DSC, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="247a3-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="247a3-115">Polecenie cmdlet Set-AzVMDscExtension ustawia tę nazwę na Microsoft. PowerShell. DSC, która jest wartością domyślną używaną przez polecenie **Remove-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="247a3-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="247a3-116">-Nowait</span><span class="sxs-lookup"><span data-stu-id="247a3-116">-NoWait</span></span>
<span data-ttu-id="247a3-117">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="247a3-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="247a3-118">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="247a3-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="247a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="247a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="247a3-120">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="247a3-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="247a3-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="247a3-121">-VMName</span></span>
<span data-ttu-id="247a3-122">Określa nazwę maszyny wirtualnej, z poziomu której to polecenie cmdlet usuwa rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="247a3-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="247a3-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="247a3-123">-Confirm</span></span>
<span data-ttu-id="247a3-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="247a3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="247a3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="247a3-125">-WhatIf</span></span>
<span data-ttu-id="247a3-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="247a3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="247a3-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="247a3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="247a3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="247a3-128">CommonParameters</span></span>
<span data-ttu-id="247a3-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="247a3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="247a3-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="247a3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="247a3-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="247a3-131">INPUTS</span></span>

### <span data-ttu-id="247a3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="247a3-132">System.String</span></span>

## <span data-ttu-id="247a3-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="247a3-133">OUTPUTS</span></span>

### <span data-ttu-id="247a3-134">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="247a3-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="247a3-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="247a3-135">NOTES</span></span>

## <span data-ttu-id="247a3-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="247a3-136">RELATED LINKS</span></span>

[<span data-ttu-id="247a3-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="247a3-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="247a3-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="247a3-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


