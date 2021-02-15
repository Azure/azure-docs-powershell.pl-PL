---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 70495ee657e511aace4babf47959c4bd6841197c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177539"
---
# <span data-ttu-id="d8f9c-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d8f9c-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="d8f9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f9c-103">Usuwa rozszerzenie z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="d8f9c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8f9c-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8f9c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8f9c-105">DESCRIPTION</span></span>
<span data-ttu-id="d8f9c-106">Polecenie **cmdlet Remove-AzVMExtension** usuwa rozszerzenie z rozszerzeń maszyny wirtualnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="d8f9c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8f9c-107">EXAMPLES</span></span>

### <span data-ttu-id="d8f9c-108">Przykład 1. Usuwanie rozszerzenia z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d8f9c-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="d8f9c-109">To polecenie usuwa rozszerzenie o nazwie Test Contoso z maszyny wirtualnej o nazwie VirtualMachine22 w grupie Zasobów11.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="d8f9c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8f9c-110">PARAMETERS</span></span>

### <span data-ttu-id="d8f9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f9c-111">-DefaultProfile</span></span>
<span data-ttu-id="d8f9c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8f9c-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d8f9c-113">-Force</span></span>
<span data-ttu-id="d8f9c-114">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d8f9c-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d8f9c-115">-Name</span></span>
<span data-ttu-id="d8f9c-116">Określa nazwę rozszerzenia, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d8f9c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f9c-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8f9c-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d8f9c-119">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="d8f9c-119">-VMName</span></span>
<span data-ttu-id="d8f9c-120">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="d8f9c-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8f9c-121">-Confirm</span></span>
<span data-ttu-id="d8f9c-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8f9c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8f9c-123">-WhatIf</span></span>
<span data-ttu-id="d8f9c-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8f9c-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8f9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f9c-126">CommonParameters</span></span>
<span data-ttu-id="d8f9c-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f9c-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8f9c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f9c-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8f9c-129">INPUTS</span></span>

### <span data-ttu-id="d8f9c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d8f9c-130">System.String</span></span>

## <span data-ttu-id="d8f9c-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8f9c-131">OUTPUTS</span></span>

### <span data-ttu-id="d8f9c-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d8f9c-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d8f9c-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8f9c-133">NOTES</span></span>

## <span data-ttu-id="d8f9c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8f9c-134">RELATED LINKS</span></span>

[<span data-ttu-id="d8f9c-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d8f9c-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="d8f9c-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d8f9c-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


