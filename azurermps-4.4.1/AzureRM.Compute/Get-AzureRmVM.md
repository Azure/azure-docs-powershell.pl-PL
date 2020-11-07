---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: afe5c168c9a5f3633ce4766df5938a81ccc60510
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716749"
---
# <span data-ttu-id="19de1-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19de1-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="19de1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19de1-102">SYNOPSIS</span></span>
<span data-ttu-id="19de1-103">Pobiera właściwości maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19de1-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19de1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19de1-104">SYNTAX</span></span>

### <span data-ttu-id="19de1-105">ListAllVirtualMachinesParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="19de1-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19de1-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="19de1-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19de1-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="19de1-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19de1-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="19de1-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19de1-109">Opis</span><span class="sxs-lookup"><span data-stu-id="19de1-109">DESCRIPTION</span></span>
<span data-ttu-id="19de1-110">Polecenie cmdlet **Get-AzureRmVM** pobiera widok modelu i widok wystąpienia maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19de1-110">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="19de1-111">Widok modelu to określone przez użytkownika właściwości maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19de1-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="19de1-112">Widok wystąpienia jest stanem poziomu wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19de1-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="19de1-113">Określ parametr *status* , aby uzyskać dostęp tylko do widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19de1-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="19de1-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19de1-114">EXAMPLES</span></span>

### <span data-ttu-id="19de1-115">Przykład 1: pobieranie właściwości widoku modelu i wystąpienia</span><span class="sxs-lookup"><span data-stu-id="19de1-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="19de1-116">To polecenie pobiera widok modelu i właściwości widoku wystąpienia maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="19de1-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="19de1-117">Przykład 2: pobieranie właściwości widoku wystąpienia</span><span class="sxs-lookup"><span data-stu-id="19de1-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="19de1-118">To polecenie pobiera właściwości maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="19de1-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="19de1-119">To polecenie określa parametr *stanu* .</span><span class="sxs-lookup"><span data-stu-id="19de1-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="19de1-120">Dlatego polecenie pobiera tylko właściwości widoku wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="19de1-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="19de1-121">Przykład 3: uzyskiwanie właściwości dla wszystkich maszyn wirtualnych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="19de1-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="19de1-122">To polecenie pobiera właściwości wszystkich maszyn wirtualnych w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="19de1-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="19de1-123">Przykład 4: pobieranie wszystkich maszyn wirtualnych w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="19de1-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="19de1-124">To polecenie umożliwia pobieranie wszystkich maszyn wirtualnych w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="19de1-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="19de1-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19de1-125">PARAMETERS</span></span>

### <span data-ttu-id="19de1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19de1-126">-DefaultProfile</span></span>
<span data-ttu-id="19de1-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19de1-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19de1-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="19de1-128">-DisplayHint</span></span>
<span data-ttu-id="19de1-129">Określa sposób wyświetlania obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19de1-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="19de1-130">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="19de1-130">Valid values are:</span></span>

<span data-ttu-id="19de1-131">--Compact: wyświetla tylko właściwości najwyższego poziomu</span><span class="sxs-lookup"><span data-stu-id="19de1-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="19de1-132">--Expand: wyświetla wszystkie właściwości na wszystkich poziomach</span><span class="sxs-lookup"><span data-stu-id="19de1-132">-- Expand: displays all properties in all levels</span></span>
```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: 
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19de1-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="19de1-133">-Name</span></span>
<span data-ttu-id="19de1-134">Określa nazwę maszyny wirtualnej, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="19de1-134">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19de1-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="19de1-135">-NextLink</span></span>
<span data-ttu-id="19de1-136">Umożliwia określenie następnego linku.</span><span class="sxs-lookup"><span data-stu-id="19de1-136">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19de1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19de1-137">-ResourceGroupName</span></span>
<span data-ttu-id="19de1-138">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="19de1-138">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19de1-139">-Status</span><span class="sxs-lookup"><span data-stu-id="19de1-139">-Status</span></span>
<span data-ttu-id="19de1-140">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19de1-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19de1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19de1-141">CommonParameters</span></span>
<span data-ttu-id="19de1-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19de1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19de1-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19de1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19de1-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19de1-144">INPUTS</span></span>

## <span data-ttu-id="19de1-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19de1-145">OUTPUTS</span></span>

## <span data-ttu-id="19de1-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19de1-146">NOTES</span></span>

## <span data-ttu-id="19de1-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19de1-147">RELATED LINKS</span></span>

[<span data-ttu-id="19de1-148">Nowe — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19de1-148">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="19de1-149">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19de1-149">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="19de1-150">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19de1-150">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="19de1-151">Start — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19de1-151">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="19de1-152">Zatrzymaj — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19de1-152">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="19de1-153">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="19de1-153">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


