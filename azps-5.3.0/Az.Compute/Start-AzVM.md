---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501831"
---
# <span data-ttu-id="b3500-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3500-101">Start-AzVM</span></span>

## <span data-ttu-id="b3500-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3500-102">SYNOPSIS</span></span>
<span data-ttu-id="b3500-103">Rozpoczynanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b3500-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="b3500-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3500-104">SYNTAX</span></span>

### <span data-ttu-id="b3500-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b3500-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3500-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b3500-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3500-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b3500-107">DESCRIPTION</span></span>
<span data-ttu-id="b3500-108">Polecenie cmdlet **Start-AzVM** rozpoczyna działanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b3500-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="b3500-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3500-109">EXAMPLES</span></span>

### <span data-ttu-id="b3500-110">Przykład 1. uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b3500-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b3500-111">To polecenie umożliwia uruchomienie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b3500-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="b3500-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3500-112">PARAMETERS</span></span>

### <span data-ttu-id="b3500-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3500-113">-AsJob</span></span>
<span data-ttu-id="b3500-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="b3500-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b3500-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3500-115">-DefaultProfile</span></span>
<span data-ttu-id="b3500-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3500-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3500-117">-ID</span><span class="sxs-lookup"><span data-stu-id="b3500-117">-Id</span></span>
<span data-ttu-id="b3500-118">Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b3500-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="b3500-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3500-119">-Name</span></span>
<span data-ttu-id="b3500-120">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b3500-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="b3500-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b3500-121">-NoWait</span></span>
<span data-ttu-id="b3500-122">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="b3500-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="b3500-123">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="b3500-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="b3500-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3500-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3500-125">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b3500-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b3500-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3500-126">-Confirm</span></span>
<span data-ttu-id="b3500-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3500-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3500-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3500-128">-WhatIf</span></span>
<span data-ttu-id="b3500-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3500-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3500-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3500-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3500-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3500-131">CommonParameters</span></span>
<span data-ttu-id="b3500-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3500-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3500-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3500-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3500-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3500-134">INPUTS</span></span>

### <span data-ttu-id="b3500-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b3500-135">System.String</span></span>

## <span data-ttu-id="b3500-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3500-136">OUTPUTS</span></span>

### <span data-ttu-id="b3500-137">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="b3500-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="b3500-138">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b3500-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b3500-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3500-139">NOTES</span></span>

## <span data-ttu-id="b3500-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3500-140">RELATED LINKS</span></span>

[<span data-ttu-id="b3500-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3500-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b3500-142">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="b3500-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="b3500-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3500-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="b3500-144">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3500-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="b3500-145">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="b3500-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="b3500-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3500-146">Update-AzVM</span></span>](./Update-AzVM.md)


