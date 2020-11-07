---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 53c9bc55c2ac8237544f293a4c42352d89681852
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706264"
---
# <span data-ttu-id="e4574-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="e4574-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="e4574-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4574-102">SYNOPSIS</span></span>
<span data-ttu-id="e4574-103">Usuwa niestandardowe rozszerzenie skryptu z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e4574-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="e4574-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4574-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4574-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4574-105">DESCRIPTION</span></span>
<span data-ttu-id="e4574-106">Polecenie cmdlet **Remove-AzVMCustomScriptExtension** usuwa rozszerzenie maszyny wirtualnej skryptu niestandardowego z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e4574-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="e4574-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4574-107">EXAMPLES</span></span>

## <span data-ttu-id="e4574-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4574-108">PARAMETERS</span></span>

### <span data-ttu-id="e4574-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4574-109">-DefaultProfile</span></span>
<span data-ttu-id="e4574-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4574-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4574-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e4574-111">-Force</span></span>
<span data-ttu-id="e4574-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e4574-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4574-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4574-113">-Name</span></span>
<span data-ttu-id="e4574-114">Określa nazwę niestandardowego rozszerzenia skryptu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4574-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4574-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e4574-115">-NoWait</span></span>
<span data-ttu-id="e4574-116">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="e4574-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e4574-117">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="e4574-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e4574-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4574-118">-ResourceGroupName</span></span>
<span data-ttu-id="e4574-119">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e4574-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e4574-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="e4574-120">-VMName</span></span>
<span data-ttu-id="e4574-121">Określa nazwę maszyny wirtualnej, z poziomu której to polecenie cmdlet usuwa niestandardowe rozszerzenie skryptu.</span><span class="sxs-lookup"><span data-stu-id="e4574-121">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4574-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4574-122">-Confirm</span></span>
<span data-ttu-id="e4574-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4574-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4574-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4574-124">-WhatIf</span></span>
<span data-ttu-id="e4574-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4574-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4574-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4574-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4574-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4574-127">CommonParameters</span></span>
<span data-ttu-id="e4574-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4574-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4574-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4574-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4574-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4574-130">INPUTS</span></span>

### <span data-ttu-id="e4574-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e4574-131">System.String</span></span>

## <span data-ttu-id="e4574-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4574-132">OUTPUTS</span></span>

### <span data-ttu-id="e4574-133">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e4574-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e4574-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4574-134">NOTES</span></span>

## <span data-ttu-id="e4574-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4574-135">RELATED LINKS</span></span>

[<span data-ttu-id="e4574-136">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="e4574-136">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="e4574-137">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="e4574-137">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
