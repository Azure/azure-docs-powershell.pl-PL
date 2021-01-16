---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: f1103e8fc7ed9646aa6b91bc0336e331f7ada990
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333997"
---
# <span data-ttu-id="796dd-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="796dd-101">Get-AzVM</span></span>

## <span data-ttu-id="796dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="796dd-102">SYNOPSIS</span></span>
<span data-ttu-id="796dd-103">Pobiera właściwości maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="796dd-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="796dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="796dd-104">SYNTAX</span></span>

### <span data-ttu-id="796dd-105">DefaultParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="796dd-105">DefaultParamSet (Default)</span></span>
```
Get-AzVM [[-ResourceGroupName] <String>] [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="796dd-106">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="796dd-106">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="796dd-107">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="796dd-107">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="796dd-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="796dd-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="796dd-109">Opis</span><span class="sxs-lookup"><span data-stu-id="796dd-109">DESCRIPTION</span></span>
<span data-ttu-id="796dd-110">Polecenie cmdlet **Get-AzVM** pobiera widok modelu lub widok wystąpienia maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="796dd-110">The **Get-AzVM** cmdlet gets the model view or the instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="796dd-111">Widok modelu to określone przez użytkownika właściwości maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="796dd-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="796dd-112">Widok wystąpienia jest stanem poziomu wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="796dd-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="796dd-113">Określ parametr *status* , aby uzyskać widok wystąpienia maszyny wirtualnej zamiast widoku modelu, który jest domyślny.</span><span class="sxs-lookup"><span data-stu-id="796dd-113">Specify the *Status* parameter to get the instance view of a virtual machine instead of the model view which is the default.</span></span>

## <span data-ttu-id="796dd-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="796dd-114">EXAMPLES</span></span>

### <span data-ttu-id="796dd-115">Przykład 1: pobieranie właściwości widoku modelu i wystąpienia</span><span class="sxs-lookup"><span data-stu-id="796dd-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"

ResourceGroupName        : ResourceGroup11
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/M
icrosoft.Compute/virtualMachines/VirtualMachine07
VmId                     : 00000000-0000-0000-0000-000000000000
Name                     : VirtualMachine07
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {"creationSource":"acs-VirtualMachine07"}
AvailabilitySetReference : {Id}
DiagnosticsProfile       : {BootDiagnostics}
Extensions               : {linuxdiagnostic, waitforleader}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, LinuxConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
```

<span data-ttu-id="796dd-116">To polecenie pobiera widok modelu i właściwości widoku wystąpienia maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="796dd-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="796dd-117">Przykład 2: pobieranie właściwości widoku wystąpienia</span><span class="sxs-lookup"><span data-stu-id="796dd-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status

ResourceGroupName       : ResourceGroup11
Name                    : VirtualMachine07
Disks[0]                :
  Name                  : VirtualMachine07-osdisk
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Time                : 3/1/2019 12:59:30 AM
Extensions[0]           :
  Name                  : linuxdiagnostic
  Type                  : Microsoft.OSTCExtensions.LinuxDiagnostic
  TypeHandlerVersion    : 2.3.9029
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Invalid config settings given: Empty storageAccountName. Install will proceed, but enable
can't proceed, in which case it's still considered a success as it's an external error.
Extensions[1]           :
  Name                  : waitforleader
  Type                  : Microsoft.OSTCExtensions.CustomScriptForLinux
  TypeHandlerVersion    : 1.5.4
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Command is finished.
---stdout---
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
PING leader.mesos (xxx.xx.x.x) 56(84) bytes of data.
64 bytes from xxx.xx.x.x: icmp_seq=1 ttl=64 time=0.022 ms

--- leader.mesos ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 0.022/0.022/0.022/0.000 ms
leader.mesos up

---errout---
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos


PlatformFaultDomain     : 0
PlatformUpdateDomain    : 0
VMAgent                 :
  VmAgentVersion        : 2.2.37
  ExtensionHandlers[0]  :
    Type                : Microsoft.OSTCExtensions.LinuxDiagnostic
    TypeHandlerVersion  : 2.3.9029
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  ExtensionHandlers[1]  :
    Type                : Microsoft.OSTCExtensions.CustomScriptForLinux
    TypeHandlerVersion  : 1.5.4
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Ready
    Message             : Guest Agent is running
    Time                : 3/1/2019 2:04:12 AM
Statuses[0]             :
  Code                  : ProvisioningState/succeeded
  Level                 : Info
  DisplayStatus         : Provisioning succeeded
  Time                  : 3/1/2019 1:01:57 AM
Statuses[1]             :
  Code                  : PowerState/running
  Level                 : Info
  DisplayStatus         : VM running
```

<span data-ttu-id="796dd-118">To polecenie pobiera właściwości maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="796dd-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="796dd-119">To polecenie określa parametr *stanu* .</span><span class="sxs-lookup"><span data-stu-id="796dd-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="796dd-120">Dlatego polecenie pobiera tylko właściwości widoku wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="796dd-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="796dd-121">Przykład 3: uzyskiwanie właściwości dla wszystkich maszyn wirtualnych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="796dd-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
ResourceGroup11     test1         eastus Standard_DS1_v2 Windows          test1
ResourceGroup11     test2         westus Standard_DS1_v2 Windows          test2
ResourceGroup11     test3         eastus Standard_DS1_v2 Windows          test3
```

<span data-ttu-id="796dd-122">To polecenie pobiera właściwości wszystkich maszyn wirtualnych w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="796dd-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="796dd-123">Przykład 4: pobieranie wszystkich maszyn wirtualnych w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="796dd-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="796dd-124">To polecenie umożliwia pobieranie wszystkich maszyn wirtualnych w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="796dd-124">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="796dd-125">Przykład 5: Pobierz wszystkie maszyny wirtualne w tej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="796dd-125">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzVM -Location "westus"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST2               test4         westus Standard_DS1_v2 Windows          test4
```

<span data-ttu-id="796dd-126">To polecenie pobiera wszystkie maszyny wirtualne w zachodnim regionie Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="796dd-126">This command gets all the virtual machines in West US region.</span></span>

### <span data-ttu-id="796dd-127">Przykład 6: pobieranie wszystkich maszyn wirtualnych przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="796dd-127">Example 6: Get all virtual machines using filtering</span></span>
```
PS C:\> Get-AzVM -Name test*

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="796dd-128">To polecenie umożliwia pobieranie wszystkich maszyn wirtualnych w subskrypcji, które zaczynają się od tekstu "test".</span><span class="sxs-lookup"><span data-stu-id="796dd-128">This command gets all the virtual machines in your subscription that start with "test".</span></span>

## <span data-ttu-id="796dd-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="796dd-129">PARAMETERS</span></span>

### <span data-ttu-id="796dd-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="796dd-130">-DefaultProfile</span></span>
<span data-ttu-id="796dd-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="796dd-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="796dd-132">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="796dd-132">-DisplayHint</span></span>
<span data-ttu-id="796dd-133">Określa sposób wyświetlania obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="796dd-133">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="796dd-134">Prawidłowe wartości to:--Compact: wyświetla tylko właściwości najwyższego poziomu--expand: wyświetla wszystkie właściwości na wszystkich poziomach.</span><span class="sxs-lookup"><span data-stu-id="796dd-134">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

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

### <span data-ttu-id="796dd-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="796dd-135">-Location</span></span>
<span data-ttu-id="796dd-136">Określa lokalizację maszyn wirtualnych, które należy wyświetlić.</span><span class="sxs-lookup"><span data-stu-id="796dd-136">Specifies a location for the virtual machines to list.</span></span>

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

### <span data-ttu-id="796dd-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="796dd-137">-Name</span></span>
<span data-ttu-id="796dd-138">Określa nazwę maszyny wirtualnej, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="796dd-138">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="796dd-139">-NextLink</span><span class="sxs-lookup"><span data-stu-id="796dd-139">-NextLink</span></span>
<span data-ttu-id="796dd-140">Umożliwia określenie następnego linku.</span><span class="sxs-lookup"><span data-stu-id="796dd-140">Specifies the next link.</span></span>

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

### <span data-ttu-id="796dd-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="796dd-141">-ResourceGroupName</span></span>
<span data-ttu-id="796dd-142">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="796dd-142">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="796dd-143">-Status</span><span class="sxs-lookup"><span data-stu-id="796dd-143">-Status</span></span>
<span data-ttu-id="796dd-144">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="796dd-144">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="796dd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="796dd-145">CommonParameters</span></span>
<span data-ttu-id="796dd-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="796dd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="796dd-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="796dd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="796dd-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="796dd-148">INPUTS</span></span>

### <span data-ttu-id="796dd-149">System. String</span><span class="sxs-lookup"><span data-stu-id="796dd-149">System.String</span></span>

### <span data-ttu-id="796dd-150">System. URI</span><span class="sxs-lookup"><span data-stu-id="796dd-150">System.Uri</span></span>

### <span data-ttu-id="796dd-151">Microsoft. Azure. Commands. COMPUTE. models. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="796dd-151">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="796dd-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="796dd-152">OUTPUTS</span></span>

### <span data-ttu-id="796dd-153">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="796dd-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="796dd-154">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="796dd-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="796dd-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="796dd-155">NOTES</span></span>

## <span data-ttu-id="796dd-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="796dd-156">RELATED LINKS</span></span>

[<span data-ttu-id="796dd-157">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="796dd-157">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="796dd-158">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="796dd-158">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="796dd-159">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="796dd-159">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="796dd-160">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="796dd-160">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="796dd-161">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="796dd-161">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="796dd-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="796dd-162">Update-AzVM</span></span>](./Update-AzVM.md)


