---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 79b16afbd6188682ff68ba5b2f2d9ccae67ff630
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177563"
---
# <span data-ttu-id="c0561-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c0561-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="c0561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0561-102">SYNOPSIS</span></span>
<span data-ttu-id="c0561-103">Usuwa rozszerzenie Naniesienie z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c0561-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="c0561-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0561-104">SYNTAX</span></span>

### <span data-ttu-id="c0561-105">Linux</span><span class="sxs-lookup"><span data-stu-id="c0561-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0561-106">Windows</span><span class="sxs-lookup"><span data-stu-id="c0561-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0561-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0561-107">DESCRIPTION</span></span>
<span data-ttu-id="c0561-108">Polecenie **cmdlet Remove-AzVMChefExtension** usuwa rozszerzenie Naniesione z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c0561-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="c0561-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0561-109">EXAMPLES</span></span>

### <span data-ttu-id="c0561-110">Przykład 1. Usunięcie rozszerzenia Dod z maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="c0561-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="c0561-111">To polecenie usuwa rozszerzenie Doc z maszyny wirtualnej opartej na systemie Windows o nazwie WindowsVM001, które należy do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="c0561-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="c0561-112">Przykład 2. Usunięcie rozszerzenia Dod z maszyny wirtualnej systemu Linux</span><span class="sxs-lookup"><span data-stu-id="c0561-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="c0561-113">To polecenie usuwa rozszerzenie na komputerze wirtualnym opartym na systemie Linux o nazwie LinuxVM001, które należy do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="c0561-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="c0561-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0561-114">PARAMETERS</span></span>

### <span data-ttu-id="c0561-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0561-115">-DefaultProfile</span></span>
<span data-ttu-id="c0561-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0561-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0561-117">— Linux</span><span class="sxs-lookup"><span data-stu-id="c0561-117">-Linux</span></span>
<span data-ttu-id="c0561-118">Wskazuje, że to polecenie cmdlet jest docelowe dla maszyny wirtualnej systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="c0561-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0561-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c0561-119">-Name</span></span>
<span data-ttu-id="c0561-120">Określa nazwę rozszerzenia Tym, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0561-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0561-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c0561-121">-NoWait</span></span>
<span data-ttu-id="c0561-122">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="c0561-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="c0561-123">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="c0561-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="c0561-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0561-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0561-125">Określa nazwę grupy zasobów zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="c0561-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="c0561-126">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="c0561-126">-VMName</span></span>
<span data-ttu-id="c0561-127">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet usuwa rozszerzenie AAD.</span><span class="sxs-lookup"><span data-stu-id="c0561-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="c0561-128">— Windows</span><span class="sxs-lookup"><span data-stu-id="c0561-128">-Windows</span></span>
<span data-ttu-id="c0561-129">Wskazuje, że to polecenie cmdlet jest docelowe dla maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="c0561-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0561-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0561-130">-Confirm</span></span>
<span data-ttu-id="c0561-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0561-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0561-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0561-132">-WhatIf</span></span>
<span data-ttu-id="c0561-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0561-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0561-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c0561-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0561-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0561-135">CommonParameters</span></span>
<span data-ttu-id="c0561-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0561-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0561-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0561-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0561-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0561-138">INPUTS</span></span>

### <span data-ttu-id="c0561-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c0561-139">System.String</span></span>

## <span data-ttu-id="c0561-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c0561-140">OUTPUTS</span></span>

### <span data-ttu-id="c0561-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c0561-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c0561-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0561-142">NOTES</span></span>

## <span data-ttu-id="c0561-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0561-143">RELATED LINKS</span></span>

[<span data-ttu-id="c0561-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c0561-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="c0561-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c0561-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
