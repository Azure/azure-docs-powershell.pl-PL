---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: f7965e43c7a294d50d6f0774f76504a90c9d7148
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893486"
---
# <span data-ttu-id="26b9f-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="26b9f-101">Restart-AzVM</span></span>

## <span data-ttu-id="26b9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="26b9f-103">Ponowne uruchamianie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="26b9f-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="26b9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26b9f-104">SYNTAX</span></span>

### <span data-ttu-id="26b9f-105">RestartResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26b9f-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26b9f-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="26b9f-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26b9f-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="26b9f-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26b9f-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="26b9f-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26b9f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="26b9f-109">DESCRIPTION</span></span>
<span data-ttu-id="26b9f-110">Polecenie cmdlet **restart-AzVM** powoduje ponowne uruchomienie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="26b9f-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="26b9f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26b9f-111">EXAMPLES</span></span>

### <span data-ttu-id="26b9f-112">Przykład 1: ponowne uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="26b9f-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="26b9f-113">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="26b9f-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="26b9f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26b9f-114">PARAMETERS</span></span>

### <span data-ttu-id="26b9f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26b9f-115">-AsJob</span></span>
<span data-ttu-id="26b9f-116">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="26b9f-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="26b9f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b9f-117">-DefaultProfile</span></span>
<span data-ttu-id="26b9f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26b9f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26b9f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="26b9f-119">-Id</span></span>
<span data-ttu-id="26b9f-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26b9f-120">The resource group name.</span></span>

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

### <span data-ttu-id="26b9f-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26b9f-121">-Name</span></span>
<span data-ttu-id="26b9f-122">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="26b9f-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="26b9f-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="26b9f-123">-PerformMaintenance</span></span>
<span data-ttu-id="26b9f-124">Aby przeprowadzić konserwację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="26b9f-124">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="26b9f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26b9f-125">-ResourceGroupName</span></span>
<span data-ttu-id="26b9f-126">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="26b9f-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="26b9f-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26b9f-127">-Confirm</span></span>
<span data-ttu-id="26b9f-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b9f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26b9f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26b9f-129">-WhatIf</span></span>
<span data-ttu-id="26b9f-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b9f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26b9f-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26b9f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26b9f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b9f-132">CommonParameters</span></span>
<span data-ttu-id="26b9f-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b9f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b9f-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b9f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b9f-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26b9f-135">INPUTS</span></span>

### <span data-ttu-id="26b9f-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="26b9f-136">None</span></span>
<span data-ttu-id="26b9f-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="26b9f-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26b9f-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26b9f-138">OUTPUTS</span></span>

### <span data-ttu-id="26b9f-139">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="26b9f-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="26b9f-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26b9f-140">NOTES</span></span>

## <span data-ttu-id="26b9f-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26b9f-141">RELATED LINKS</span></span>

[<span data-ttu-id="26b9f-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="26b9f-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="26b9f-143">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="26b9f-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="26b9f-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="26b9f-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="26b9f-145">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="26b9f-145">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="26b9f-146">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="26b9f-146">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="26b9f-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="26b9f-147">Update-AzVM</span></span>](./Update-AzVM.md)


