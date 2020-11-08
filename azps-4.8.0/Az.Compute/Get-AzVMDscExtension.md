---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: ba4ac8d48c72ffac164e447777670c48f529f68f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062896"
---
# <span data-ttu-id="ed4c6-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ed4c6-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="ed4c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed4c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ed4c6-103">Pobiera ustawienia rozszerzenia DSC na określonej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ed4c6-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="ed4c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed4c6-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed4c6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ed4c6-105">DESCRIPTION</span></span>
<span data-ttu-id="ed4c6-106">Polecenie cmdlet **Get-AzVMDscExtension** pobiera ustawienia żądanego rozszerzenia konfiguracji stanu (DSC) na konkretnej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ed4c6-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="ed4c6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed4c6-107">EXAMPLES</span></span>

### <span data-ttu-id="ed4c6-108">Przykład 1: uzyskiwanie ustawień rozszerzenia DSC</span><span class="sxs-lookup"><span data-stu-id="ed4c6-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="ed4c6-109">To polecenie uzyskuje ustawienia dotyczące rozszerzenia o nazwie DSC na maszynie wirtualnej o nazwie VM07.</span><span class="sxs-lookup"><span data-stu-id="ed4c6-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="ed4c6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed4c6-110">PARAMETERS</span></span>

### <span data-ttu-id="ed4c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed4c6-111">-DefaultProfile</span></span>
<span data-ttu-id="ed4c6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed4c6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed4c6-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed4c6-113">-Name</span></span>
<span data-ttu-id="ed4c6-114">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="ed4c6-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="ed4c6-115">Polecenie cmdlet Set-AzVMDscExtension powoduje ustawienie tej nazwy na Microsoft. PowerShell. DSC, która jest taka sama, jak wartość używana przez polecenie **Get-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="ed4c6-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="ed4c6-116">Ten parametr należy określić tylko w przypadku zmiany nazwy domyślnej w poleceniu cmdlet **Set-AzVMDscExtension** lub użycia innej nazwy zasobu w szablonie Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="ed4c6-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed4c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed4c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="ed4c6-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ed4c6-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ed4c6-119">-Status</span><span class="sxs-lookup"><span data-stu-id="ed4c6-119">-Status</span></span>
<span data-ttu-id="ed4c6-120">Wskazuje, że to polecenie cmdlet pobiera widok wystąpienia rozszerzenia DSC.</span><span class="sxs-lookup"><span data-stu-id="ed4c6-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="ed4c6-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="ed4c6-121">-VMName</span></span>
<span data-ttu-id="ed4c6-122">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="ed4c6-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="ed4c6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed4c6-123">CommonParameters</span></span>
<span data-ttu-id="ed4c6-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed4c6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed4c6-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed4c6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed4c6-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed4c6-126">INPUTS</span></span>

### <span data-ttu-id="ed4c6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ed4c6-127">System.String</span></span>

### <span data-ttu-id="ed4c6-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ed4c6-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ed4c6-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed4c6-129">OUTPUTS</span></span>

### <span data-ttu-id="ed4c6-130">Microsoft. Azure. Commands. COMPUTE. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="ed4c6-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="ed4c6-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed4c6-131">NOTES</span></span>

## <span data-ttu-id="ed4c6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed4c6-132">RELATED LINKS</span></span>

[<span data-ttu-id="ed4c6-133">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ed4c6-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="ed4c6-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ed4c6-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


