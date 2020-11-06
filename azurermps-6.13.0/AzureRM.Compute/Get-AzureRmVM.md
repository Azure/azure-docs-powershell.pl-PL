---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: 8601a7cc6a02211a0264030784485a5ecb4d29fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541864"
---
# <span data-ttu-id="a90e3-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a90e3-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="a90e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a90e3-102">SYNOPSIS</span></span>
<span data-ttu-id="a90e3-103">Pobiera właściwości maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a90e3-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a90e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a90e3-104">SYNTAX</span></span>

### <span data-ttu-id="a90e3-105">ListAllVirtualMachinesParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a90e3-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a90e3-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="a90e3-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a90e3-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="a90e3-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a90e3-108">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="a90e3-108">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a90e3-109">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="a90e3-109">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a90e3-110">Opis</span><span class="sxs-lookup"><span data-stu-id="a90e3-110">DESCRIPTION</span></span>
<span data-ttu-id="a90e3-111">Polecenie cmdlet **Get-AzureRmVM** pobiera widok modelu i widok wystąpienia maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a90e3-111">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="a90e3-112">Widok modelu to określone przez użytkownika właściwości maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a90e3-112">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="a90e3-113">Widok wystąpienia jest stanem poziomu wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a90e3-113">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="a90e3-114">Określ parametr *status* , aby uzyskać dostęp tylko do widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a90e3-114">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="a90e3-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a90e3-115">EXAMPLES</span></span>

### <span data-ttu-id="a90e3-116">Przykład 1: pobieranie właściwości widoku modelu i wystąpienia</span><span class="sxs-lookup"><span data-stu-id="a90e3-116">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="a90e3-117">To polecenie pobiera widok modelu i właściwości widoku wystąpienia maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="a90e3-117">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="a90e3-118">Przykład 2: pobieranie właściwości widoku wystąpienia</span><span class="sxs-lookup"><span data-stu-id="a90e3-118">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="a90e3-119">To polecenie pobiera właściwości maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="a90e3-119">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="a90e3-120">To polecenie określa parametr *stanu* .</span><span class="sxs-lookup"><span data-stu-id="a90e3-120">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="a90e3-121">Dlatego polecenie pobiera tylko właściwości widoku wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="a90e3-121">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="a90e3-122">Przykład 3: uzyskiwanie właściwości dla wszystkich maszyn wirtualnych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a90e3-122">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="a90e3-123">To polecenie pobiera właściwości wszystkich maszyn wirtualnych w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a90e3-123">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="a90e3-124">Przykład 4: pobieranie wszystkich maszyn wirtualnych w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a90e3-124">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="a90e3-125">To polecenie umożliwia pobieranie wszystkich maszyn wirtualnych w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a90e3-125">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="a90e3-126">Przykład 5: Pobierz wszystkie maszyny wirtualne w tej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a90e3-126">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzureRmVM -Location "westus"
```

<span data-ttu-id="a90e3-127">To polecenie pobiera wszystkie maszyny wirtualne w zachodnim regionie Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="a90e3-127">This command gets all the virtual machines in West US region.</span></span>

## <span data-ttu-id="a90e3-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a90e3-128">PARAMETERS</span></span>

### <span data-ttu-id="a90e3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a90e3-129">-DefaultProfile</span></span>
<span data-ttu-id="a90e3-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a90e3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a90e3-131">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="a90e3-131">-DisplayHint</span></span>
<span data-ttu-id="a90e3-132">Określa sposób wyświetlania obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a90e3-132">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="a90e3-133">Prawidłowe wartości to:--Compact: wyświetla tylko właściwości najwyższego poziomu--expand: wyświetla wszystkie właściwości na wszystkich poziomach.</span><span class="sxs-lookup"><span data-stu-id="a90e3-133">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

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

### <span data-ttu-id="a90e3-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a90e3-134">-Location</span></span>
<span data-ttu-id="a90e3-135">Określa lokalizację maszyn wirtualnych, które należy wyświetlić.</span><span class="sxs-lookup"><span data-stu-id="a90e3-135">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a90e3-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a90e3-136">-Name</span></span>
<span data-ttu-id="a90e3-137">Określa nazwę maszyny wirtualnej, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="a90e3-137">Specifies the name of the virtual machine to get.</span></span>

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

### <span data-ttu-id="a90e3-138">-NextLink</span><span class="sxs-lookup"><span data-stu-id="a90e3-138">-NextLink</span></span>
<span data-ttu-id="a90e3-139">Umożliwia określenie następnego linku.</span><span class="sxs-lookup"><span data-stu-id="a90e3-139">Specifies the next link.</span></span>

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

### <span data-ttu-id="a90e3-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a90e3-140">-ResourceGroupName</span></span>
<span data-ttu-id="a90e3-141">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a90e3-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a90e3-142">-Status</span><span class="sxs-lookup"><span data-stu-id="a90e3-142">-Status</span></span>
<span data-ttu-id="a90e3-143">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a90e3-143">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="a90e3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a90e3-144">CommonParameters</span></span>
<span data-ttu-id="a90e3-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a90e3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a90e3-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a90e3-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a90e3-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a90e3-147">INPUTS</span></span>

### <span data-ttu-id="a90e3-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a90e3-148">System.String</span></span>

### <span data-ttu-id="a90e3-149">System. URI</span><span class="sxs-lookup"><span data-stu-id="a90e3-149">System.Uri</span></span>

### <span data-ttu-id="a90e3-150">Microsoft. Azure. Commands. COMPUTE. models. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="a90e3-150">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="a90e3-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a90e3-151">OUTPUTS</span></span>

### <span data-ttu-id="a90e3-152">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a90e3-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a90e3-153">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="a90e3-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="a90e3-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a90e3-154">NOTES</span></span>

## <span data-ttu-id="a90e3-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a90e3-155">RELATED LINKS</span></span>

[<span data-ttu-id="a90e3-156">Nowe — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a90e3-156">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="a90e3-157">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a90e3-157">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="a90e3-158">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a90e3-158">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="a90e3-159">Start — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a90e3-159">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="a90e3-160">Zatrzymaj — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a90e3-160">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="a90e3-161">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a90e3-161">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


