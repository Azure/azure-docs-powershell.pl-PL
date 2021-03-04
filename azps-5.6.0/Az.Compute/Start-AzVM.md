---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: daf1a9c738e6e4d0d97a22eedc8355750d15ec72
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004529"
---
# <span data-ttu-id="29957-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="29957-101">Start-AzVM</span></span>

## <span data-ttu-id="29957-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29957-102">SYNOPSIS</span></span>
<span data-ttu-id="29957-103">Uruchamia maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="29957-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="29957-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="29957-104">SYNTAX</span></span>

### <span data-ttu-id="29957-105">ResourceGroupNameParameterSetName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="29957-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29957-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="29957-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29957-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="29957-107">DESCRIPTION</span></span>
<span data-ttu-id="29957-108">Polecenie **cmdlet Start-AzVM** uruchamia maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="29957-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="29957-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="29957-109">EXAMPLES</span></span>

### <span data-ttu-id="29957-110">Przykład 1. Uruchamianie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="29957-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="29957-111">To polecenie uruchamia maszynę wirtualną o nazwie VirtualMachine07 w grupie Zasobów11.</span><span class="sxs-lookup"><span data-stu-id="29957-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="29957-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29957-112">PARAMETERS</span></span>

### <span data-ttu-id="29957-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="29957-113">-AsJob</span></span>
<span data-ttu-id="29957-114">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="29957-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="29957-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29957-115">-DefaultProfile</span></span>
<span data-ttu-id="29957-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="29957-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29957-117">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="29957-117">-Id</span></span>
<span data-ttu-id="29957-118">Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="29957-118">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29957-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="29957-119">-Name</span></span>
<span data-ttu-id="29957-120">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="29957-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29957-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="29957-121">-NoWait</span></span>
<span data-ttu-id="29957-122">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="29957-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="29957-123">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="29957-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="29957-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29957-124">-ResourceGroupName</span></span>
<span data-ttu-id="29957-125">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="29957-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29957-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29957-126">-Confirm</span></span>
<span data-ttu-id="29957-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="29957-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29957-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29957-128">-WhatIf</span></span>
<span data-ttu-id="29957-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29957-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29957-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="29957-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29957-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29957-131">CommonParameters</span></span>
<span data-ttu-id="29957-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29957-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29957-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29957-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29957-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29957-134">INPUTS</span></span>

### <span data-ttu-id="29957-135">System.String</span><span class="sxs-lookup"><span data-stu-id="29957-135">System.String</span></span>

## <span data-ttu-id="29957-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29957-136">OUTPUTS</span></span>

### <span data-ttu-id="29957-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="29957-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="29957-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="29957-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="29957-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="29957-139">NOTES</span></span>

## <span data-ttu-id="29957-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29957-140">RELATED LINKS</span></span>

[<span data-ttu-id="29957-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="29957-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="29957-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="29957-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="29957-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="29957-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="29957-144">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="29957-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="29957-145">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="29957-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="29957-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="29957-146">Update-AzVM</span></span>](./Update-AzVM.md)


