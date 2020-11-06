---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: 5fcb99a6e909675b47d245755ffd42e3c058a37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541803"
---
# <span data-ttu-id="16f87-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16f87-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="16f87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16f87-102">SYNOPSIS</span></span>
<span data-ttu-id="16f87-103">Ustawia określone akcje na określonym VMSS.</span><span class="sxs-lookup"><span data-stu-id="16f87-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16f87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16f87-104">SYNTAX</span></span>

### <span data-ttu-id="16f87-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="16f87-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f87-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="16f87-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f87-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="16f87-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f87-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="16f87-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16f87-109">Opis</span><span class="sxs-lookup"><span data-stu-id="16f87-109">DESCRIPTION</span></span>
<span data-ttu-id="16f87-110">Polecenie cmdlet **Set-AzureRmVmss** ustawia określone akcje na zestawie skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="16f87-110">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="16f87-111">Jedyna akcja obsługiwana przez ten aplet polecenia to Reimage.</span><span class="sxs-lookup"><span data-stu-id="16f87-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="16f87-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16f87-112">EXAMPLES</span></span>

### <span data-ttu-id="16f87-113">Przykład 1: odobrazowanie VMSS</span><span class="sxs-lookup"><span data-stu-id="16f87-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="16f87-114">To polecenie powoduje ponowne zdjęcie VMSS o nazwie ContosoVMSS należącej do grupy zasobów o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="16f87-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="16f87-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16f87-115">PARAMETERS</span></span>

### <span data-ttu-id="16f87-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16f87-116">-AsJob</span></span>
<span data-ttu-id="16f87-117">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="16f87-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="16f87-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f87-118">-DefaultProfile</span></span>
<span data-ttu-id="16f87-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16f87-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f87-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="16f87-120">-InstanceId</span></span>
<span data-ttu-id="16f87-121">Identyfikator wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="16f87-121">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f87-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="16f87-122">-PerformMaintenance</span></span>
<span data-ttu-id="16f87-123">Wskazuje, że to polecenie cmdlet przeprowadza konserwację co najmniej jednej maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="16f87-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f87-124">-Deploy</span><span class="sxs-lookup"><span data-stu-id="16f87-124">-Redeploy</span></span>
<span data-ttu-id="16f87-125">Wskazuje, że polecenie cmdlet powoduje ponowne wdrożenie co najmniej jednej maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="16f87-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f87-126">-Reimage</span><span class="sxs-lookup"><span data-stu-id="16f87-126">-Reimage</span></span>
<span data-ttu-id="16f87-127">Wskazuje, że polecenie cmdlet reobrazuje VMSS.</span><span class="sxs-lookup"><span data-stu-id="16f87-127">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f87-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="16f87-128">-ReimageAll</span></span>
<span data-ttu-id="16f87-129">Wskazuje, że polecenie cmdlet reobrazuje wszystkie dyski w VMSS.</span><span class="sxs-lookup"><span data-stu-id="16f87-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f87-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16f87-130">-ResourceGroupName</span></span>
<span data-ttu-id="16f87-131">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="16f87-131">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="16f87-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="16f87-132">-VMScaleSetName</span></span>
<span data-ttu-id="16f87-133">Gatunek nazwa VMSS, dla którego to polecenie cmdlet ustawia akcje.</span><span class="sxs-lookup"><span data-stu-id="16f87-133">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f87-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16f87-134">-Confirm</span></span>
<span data-ttu-id="16f87-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16f87-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16f87-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16f87-136">-WhatIf</span></span>
<span data-ttu-id="16f87-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16f87-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16f87-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="16f87-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16f87-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f87-139">CommonParameters</span></span>
<span data-ttu-id="16f87-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16f87-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f87-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16f87-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f87-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16f87-142">INPUTS</span></span>

### <span data-ttu-id="16f87-143">System. String</span><span class="sxs-lookup"><span data-stu-id="16f87-143">System.String</span></span>

### <span data-ttu-id="16f87-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="16f87-144">System.String[]</span></span>

## <span data-ttu-id="16f87-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16f87-145">OUTPUTS</span></span>

### <span data-ttu-id="16f87-146">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="16f87-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="16f87-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16f87-147">NOTES</span></span>

## <span data-ttu-id="16f87-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16f87-148">RELATED LINKS</span></span>

[<span data-ttu-id="16f87-149">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16f87-149">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="16f87-150">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16f87-150">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="16f87-151">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16f87-151">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="16f87-152">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16f87-152">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="16f87-153">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16f87-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="16f87-154">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16f87-154">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="16f87-155">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16f87-155">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


