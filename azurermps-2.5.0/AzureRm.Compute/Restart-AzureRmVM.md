---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86fb5997c93aecbaa5aabd07255ae6bde840e91f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899141"
---
# <span data-ttu-id="50cf2-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="50cf2-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="50cf2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="50cf2-103">Ponowne uruchamianie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="50cf2-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50cf2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50cf2-104">SYNTAX</span></span>

### <span data-ttu-id="50cf2-105">RestartResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="50cf2-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50cf2-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="50cf2-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50cf2-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="50cf2-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50cf2-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="50cf2-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50cf2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="50cf2-109">DESCRIPTION</span></span>
<span data-ttu-id="50cf2-110">Polecenie cmdlet **restart-AzureRmVM** powoduje ponowne uruchomienie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="50cf2-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="50cf2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50cf2-111">EXAMPLES</span></span>

### <span data-ttu-id="50cf2-112">Przykład 1: ponowne uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="50cf2-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="50cf2-113">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="50cf2-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="50cf2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50cf2-114">PARAMETERS</span></span>

### <span data-ttu-id="50cf2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50cf2-115">-AsJob</span></span>
<span data-ttu-id="50cf2-116">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="50cf2-116">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50cf2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50cf2-117">-DefaultProfile</span></span>
<span data-ttu-id="50cf2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50cf2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50cf2-119">-ID</span><span class="sxs-lookup"><span data-stu-id="50cf2-119">-Id</span></span>
<span data-ttu-id="50cf2-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="50cf2-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50cf2-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50cf2-121">-Name</span></span>
<span data-ttu-id="50cf2-122">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="50cf2-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50cf2-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="50cf2-123">-PerformMaintenance</span></span>
<span data-ttu-id="50cf2-124">Aby przeprowadzić konserwację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="50cf2-124">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50cf2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50cf2-125">-ResourceGroupName</span></span>
<span data-ttu-id="50cf2-126">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="50cf2-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50cf2-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50cf2-127">-Confirm</span></span>
<span data-ttu-id="50cf2-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50cf2-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50cf2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50cf2-129">-WhatIf</span></span>
<span data-ttu-id="50cf2-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50cf2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50cf2-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="50cf2-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50cf2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50cf2-132">CommonParameters</span></span>
<span data-ttu-id="50cf2-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50cf2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50cf2-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50cf2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50cf2-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50cf2-135">INPUTS</span></span>

### <span data-ttu-id="50cf2-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="50cf2-136">None</span></span>
<span data-ttu-id="50cf2-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="50cf2-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="50cf2-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50cf2-138">OUTPUTS</span></span>

### <span data-ttu-id="50cf2-139">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="50cf2-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="50cf2-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50cf2-140">NOTES</span></span>

## <span data-ttu-id="50cf2-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50cf2-141">RELATED LINKS</span></span>

[<span data-ttu-id="50cf2-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="50cf2-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="50cf2-143">Nowe — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="50cf2-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="50cf2-144">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="50cf2-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="50cf2-145">Start — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="50cf2-145">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="50cf2-146">Zatrzymaj — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="50cf2-146">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="50cf2-147">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="50cf2-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


