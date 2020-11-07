---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: d2e9ad0d83c573292996b65924ab7078368d328f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718377"
---
# <span data-ttu-id="17635-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="17635-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="17635-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17635-102">SYNOPSIS</span></span>
<span data-ttu-id="17635-103">Pobiera właściwości VMSS.</span><span class="sxs-lookup"><span data-stu-id="17635-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17635-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17635-104">SYNTAX</span></span>

### <span data-ttu-id="17635-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="17635-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17635-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="17635-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17635-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="17635-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17635-108">Opis</span><span class="sxs-lookup"><span data-stu-id="17635-108">DESCRIPTION</span></span>
<span data-ttu-id="17635-109">Polecenie cmdlet **Get-AzureRmVmss** umożliwia wyświetlenie modelu i widoku wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="17635-109">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="17635-110">Widok modelu to określone przez użytkownika właściwości zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17635-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="17635-111">Widok wystąpienia jest stanem poziomu wystąpienia zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17635-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="17635-112">Określ parametr *InstanceView* , aby uzyskać tylko widok wystąpienia skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17635-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="17635-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17635-113">EXAMPLES</span></span>

### <span data-ttu-id="17635-114">Przykład 1: uzyskiwanie właściwości VMSS</span><span class="sxs-lookup"><span data-stu-id="17635-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="17635-115">To polecenie pobiera właściwości VMSS o nazwie VMSS001 należące do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="17635-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="17635-116">Ponieważ polecenie nie określa parametru przełącznika *InstanceView* , funkcja cmdlet pobiera widok modelu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17635-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

## <span data-ttu-id="17635-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17635-117">PARAMETERS</span></span>

### <span data-ttu-id="17635-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17635-118">-DefaultProfile</span></span>
<span data-ttu-id="17635-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17635-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17635-120">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="17635-120">-InstanceView</span></span>
<span data-ttu-id="17635-121">Wskazuje, że ten aplet polecenia pobiera tylko widok skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17635-121">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="17635-122">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="17635-122">-OSUpgradeHistory</span></span>
<span data-ttu-id="17635-123">Wskazuje, że to polecenie cmdlet wyświetla historię uaktualnienia systemu operacyjnego zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17635-123">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17635-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17635-124">-ResourceGroupName</span></span>
<span data-ttu-id="17635-125">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="17635-125">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17635-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="17635-126">-VMScaleSetName</span></span>
<span data-ttu-id="17635-127">Gatunek nazwy VMSS.</span><span class="sxs-lookup"><span data-stu-id="17635-127">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17635-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17635-128">CommonParameters</span></span>
<span data-ttu-id="17635-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17635-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17635-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17635-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17635-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17635-131">INPUTS</span></span>

### <span data-ttu-id="17635-132">System. String</span><span class="sxs-lookup"><span data-stu-id="17635-132">System.String</span></span>

## <span data-ttu-id="17635-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17635-133">OUTPUTS</span></span>

### <span data-ttu-id="17635-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17635-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="17635-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17635-135">NOTES</span></span>

## <span data-ttu-id="17635-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17635-136">RELATED LINKS</span></span>

[<span data-ttu-id="17635-137">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="17635-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="17635-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="17635-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="17635-139">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="17635-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="17635-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="17635-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="17635-141">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="17635-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="17635-142">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="17635-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="17635-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="17635-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


