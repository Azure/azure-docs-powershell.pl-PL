---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: e487e86c26ec09d1335ee34dab56292b564169b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501913"
---
# <span data-ttu-id="73070-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="73070-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="73070-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73070-102">SYNOPSIS</span></span>
<span data-ttu-id="73070-103">Pobiera ustawienia rozszerzenia DSC na określonej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="73070-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="73070-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73070-104">SYNTAX</span></span>

### <span data-ttu-id="73070-105">GetDscExtension (domyślny)</span><span class="sxs-lookup"><span data-stu-id="73070-105">GetDscExtension (Default)</span></span>
```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73070-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="73070-106">VMParameterSet</span></span>
```
Get-AzVMDscExtension [-Status] [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73070-107">Opis</span><span class="sxs-lookup"><span data-stu-id="73070-107">DESCRIPTION</span></span>
<span data-ttu-id="73070-108">Polecenie cmdlet **Get-AzVMDscExtension** pobiera ustawienia żądanego rozszerzenia konfiguracji stanu (DSC) na konkretnej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="73070-108">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="73070-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73070-109">EXAMPLES</span></span>

### <span data-ttu-id="73070-110">Przykład 1: uzyskiwanie ustawień rozszerzenia DSC</span><span class="sxs-lookup"><span data-stu-id="73070-110">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="73070-111">To polecenie uzyskuje ustawienia dotyczące rozszerzenia o nazwie DSC na maszynie wirtualnej o nazwie VM07.</span><span class="sxs-lookup"><span data-stu-id="73070-111">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="73070-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73070-112">PARAMETERS</span></span>

### <span data-ttu-id="73070-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73070-113">-DefaultProfile</span></span>
<span data-ttu-id="73070-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73070-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73070-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="73070-115">-Name</span></span>
<span data-ttu-id="73070-116">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="73070-116">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="73070-117">Polecenie cmdlet Set-AzVMDscExtension powoduje ustawienie tej nazwy na Microsoft. PowerShell. DSC, która jest taka sama, jak wartość używana przez polecenie **Get-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="73070-117">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="73070-118">Ten parametr należy określić tylko w przypadku zmiany nazwy domyślnej w poleceniu cmdlet **Set-AzVMDscExtension** lub użycia innej nazwy zasobu w szablonie Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="73070-118">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73070-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73070-119">-ResourceGroupName</span></span>
<span data-ttu-id="73070-120">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="73070-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73070-121">-Status</span><span class="sxs-lookup"><span data-stu-id="73070-121">-Status</span></span>
<span data-ttu-id="73070-122">Wskazuje, że to polecenie cmdlet pobiera widok wystąpienia rozszerzenia DSC.</span><span class="sxs-lookup"><span data-stu-id="73070-122">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73070-123">-VM</span><span class="sxs-lookup"><span data-stu-id="73070-123">-VM</span></span>
<span data-ttu-id="73070-124">Określa obiekt maszyny wirtualnej, na którym znajduje się rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="73070-124">Specifies the virtual machine object the extension is on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73070-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="73070-125">-VMName</span></span>
<span data-ttu-id="73070-126">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="73070-126">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73070-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73070-127">CommonParameters</span></span>
<span data-ttu-id="73070-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73070-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73070-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73070-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73070-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73070-130">INPUTS</span></span>

### <span data-ttu-id="73070-131">System. String</span><span class="sxs-lookup"><span data-stu-id="73070-131">System.String</span></span>

### <span data-ttu-id="73070-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="73070-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="73070-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73070-133">OUTPUTS</span></span>

### <span data-ttu-id="73070-134">Microsoft. Azure. Commands. COMPUTE. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="73070-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="73070-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73070-135">NOTES</span></span>

## <span data-ttu-id="73070-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73070-136">RELATED LINKS</span></span>

[<span data-ttu-id="73070-137">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="73070-137">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="73070-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="73070-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


