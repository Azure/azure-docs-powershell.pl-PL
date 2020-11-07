---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 2f33b0dbee4f584553eac1047471adef08e3523b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893789"
---
# <span data-ttu-id="18af2-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="18af2-101">Get-AzVM</span></span>

## <span data-ttu-id="18af2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18af2-102">SYNOPSIS</span></span>
<span data-ttu-id="18af2-103">Pobiera właściwości maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18af2-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="18af2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18af2-104">SYNTAX</span></span>

### <span data-ttu-id="18af2-105">ListAllVirtualMachinesParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="18af2-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18af2-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="18af2-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18af2-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="18af2-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18af2-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="18af2-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18af2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="18af2-109">DESCRIPTION</span></span>
<span data-ttu-id="18af2-110">Polecenie cmdlet **Get-AzVM** pobiera widok modelu i widok wystąpienia maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="18af2-110">The **Get-AzVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="18af2-111">Widok modelu to określone przez użytkownika właściwości maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18af2-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="18af2-112">Widok wystąpienia jest stanem poziomu wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18af2-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="18af2-113">Określ parametr *status* , aby uzyskać dostęp tylko do widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18af2-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="18af2-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18af2-114">EXAMPLES</span></span>

### <span data-ttu-id="18af2-115">Przykład 1: pobieranie właściwości widoku modelu i wystąpienia</span><span class="sxs-lookup"><span data-stu-id="18af2-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="18af2-116">To polecenie pobiera widok modelu i właściwości widoku wystąpienia maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="18af2-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="18af2-117">Przykład 2: pobieranie właściwości widoku wystąpienia</span><span class="sxs-lookup"><span data-stu-id="18af2-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="18af2-118">To polecenie pobiera właściwości maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="18af2-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="18af2-119">To polecenie określa parametr *stanu* .</span><span class="sxs-lookup"><span data-stu-id="18af2-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="18af2-120">Dlatego polecenie pobiera tylko właściwości widoku wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="18af2-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="18af2-121">Przykład 3: uzyskiwanie właściwości dla wszystkich maszyn wirtualnych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="18af2-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="18af2-122">To polecenie pobiera właściwości wszystkich maszyn wirtualnych w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="18af2-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="18af2-123">Przykład 4: pobieranie wszystkich maszyn wirtualnych w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="18af2-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM
```

<span data-ttu-id="18af2-124">To polecenie umożliwia pobieranie wszystkich maszyn wirtualnych w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="18af2-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="18af2-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18af2-125">PARAMETERS</span></span>

### <span data-ttu-id="18af2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18af2-126">-DefaultProfile</span></span>
<span data-ttu-id="18af2-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18af2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18af2-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="18af2-128">-DisplayHint</span></span>
<span data-ttu-id="18af2-129">Określa sposób wyświetlania obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18af2-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="18af2-130">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="18af2-130">Valid values are:</span></span>

<span data-ttu-id="18af2-131">--Compact: wyświetla tylko właściwości najwyższego poziomu</span><span class="sxs-lookup"><span data-stu-id="18af2-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="18af2-132">--Expand: wyświetla wszystkie właściwości na wszystkich poziomach</span><span class="sxs-lookup"><span data-stu-id="18af2-132">-- Expand: displays all properties in all levels</span></span>
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: 
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18af2-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="18af2-133">-Name</span></span>
<span data-ttu-id="18af2-134">Określa nazwę maszyny wirtualnej, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="18af2-134">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18af2-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="18af2-135">-NextLink</span></span>
<span data-ttu-id="18af2-136">Umożliwia określenie następnego linku.</span><span class="sxs-lookup"><span data-stu-id="18af2-136">Specifies the next link.</span></span>

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18af2-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18af2-137">-ResourceGroupName</span></span>
<span data-ttu-id="18af2-138">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="18af2-138">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18af2-139">-Status</span><span class="sxs-lookup"><span data-stu-id="18af2-139">-Status</span></span>
<span data-ttu-id="18af2-140">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18af2-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18af2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18af2-141">CommonParameters</span></span>
<span data-ttu-id="18af2-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18af2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18af2-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18af2-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18af2-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18af2-144">INPUTS</span></span>

### <span data-ttu-id="18af2-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="18af2-145">None</span></span>
<span data-ttu-id="18af2-146">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="18af2-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18af2-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18af2-147">OUTPUTS</span></span>

### <span data-ttu-id="18af2-148">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="18af2-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="18af2-149">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="18af2-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="18af2-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18af2-150">NOTES</span></span>

## <span data-ttu-id="18af2-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18af2-151">RELATED LINKS</span></span>

[<span data-ttu-id="18af2-152">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="18af2-152">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="18af2-153">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="18af2-153">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="18af2-154">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="18af2-154">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="18af2-155">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="18af2-155">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="18af2-156">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="18af2-156">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="18af2-157">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="18af2-157">Update-AzVM</span></span>](./Update-AzVM.md)


