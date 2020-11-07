---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: f861465fcc9f27f71142ffd4e49935039f3da9c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706405"
---
# <span data-ttu-id="93a84-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="93a84-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="93a84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93a84-102">SYNOPSIS</span></span>
<span data-ttu-id="93a84-103">Pobiera właściwości rozszerzeń maszyny wirtualnej zainstalowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="93a84-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="93a84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93a84-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93a84-105">Opis</span><span class="sxs-lookup"><span data-stu-id="93a84-105">DESCRIPTION</span></span>
<span data-ttu-id="93a84-106">Polecenie cmdlet **Get-AzVMExtension** pobiera właściwości rozszerzeń maszyny wirtualnej zainstalowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="93a84-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="93a84-107">Określ nazwę rozszerzenia, dla którego chcesz uzyskać właściwości.</span><span class="sxs-lookup"><span data-stu-id="93a84-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="93a84-108">Aby uzyskać tylko widok wystąpienia rozszerzenia, określ parametr status.</span><span class="sxs-lookup"><span data-stu-id="93a84-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="93a84-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93a84-109">EXAMPLES</span></span>

### <span data-ttu-id="93a84-110">Przykład 1: uzyskiwanie właściwości rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="93a84-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="93a84-111">To polecenie pobiera właściwości rozszerzenia o nazwie CustomScriptExtension na maszynie wirtualnej o nazwie VirtualMachine22 w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="93a84-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="93a84-112">Przykład 2: pobieranie widoku wystąpienia rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="93a84-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                : {Microsoft.Azure.Management.Compute.Models.InstanceViewStatus}
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="93a84-113">To polecenie uzyskuje widok wystąpienia dla rozszerzenia o nazwie CustomScriptExtension na maszynie wirtualnej o nazwie VirtualMachine22 w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="93a84-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="93a84-114">Przykład 3: pobieranie wszystkich rozszerzeń zainstalowanych na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="93a84-114">Example 3: Get all extensions installed on a VM</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="93a84-115">To polecenie powoduje wyświetlenie listy rozszerzeń zainstalowanych na maszynie wirtualnej o nazwie VirtualMachine22 w ResourceGroup11 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="93a84-115">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="93a84-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93a84-116">PARAMETERS</span></span>

### <span data-ttu-id="93a84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a84-117">-DefaultProfile</span></span>
<span data-ttu-id="93a84-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="93a84-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93a84-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="93a84-119">-Name</span></span>
<span data-ttu-id="93a84-120">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="93a84-120">Specifies the name of an extension.</span></span>
<span data-ttu-id="93a84-121">To polecenie cmdlet umożliwia pobieranie właściwości rozszerzenia, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="93a84-121">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a84-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93a84-122">-ResourceGroupName</span></span>
<span data-ttu-id="93a84-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="93a84-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a84-124">-Status</span><span class="sxs-lookup"><span data-stu-id="93a84-124">-Status</span></span>
<span data-ttu-id="93a84-125">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="93a84-125">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a84-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="93a84-126">-VMName</span></span>
<span data-ttu-id="93a84-127">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="93a84-127">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="93a84-128">To polecenie cmdlet pobiera właściwości rozszerzenia z maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="93a84-128">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a84-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a84-129">CommonParameters</span></span>
<span data-ttu-id="93a84-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93a84-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a84-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93a84-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a84-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93a84-132">INPUTS</span></span>

### <span data-ttu-id="93a84-133">System. String</span><span class="sxs-lookup"><span data-stu-id="93a84-133">System.String</span></span>

### <span data-ttu-id="93a84-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="93a84-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="93a84-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93a84-135">OUTPUTS</span></span>

### <span data-ttu-id="93a84-136">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="93a84-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="93a84-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93a84-137">NOTES</span></span>

## <span data-ttu-id="93a84-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93a84-138">RELATED LINKS</span></span>

[<span data-ttu-id="93a84-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="93a84-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="93a84-140">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="93a84-140">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


