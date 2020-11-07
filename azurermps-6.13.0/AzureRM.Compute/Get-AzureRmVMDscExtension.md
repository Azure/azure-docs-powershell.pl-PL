---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDscExtension.md
ms.openlocfilehash: 6bab7e7bc823008d018d53f146aec54f599f63d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717929"
---
# <span data-ttu-id="eaa7c-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="eaa7c-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="eaa7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eaa7c-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa7c-103">Pobiera ustawienia rozszerzenia DSC na określonej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eaa7c-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaa7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eaa7c-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaa7c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eaa7c-105">DESCRIPTION</span></span>
<span data-ttu-id="eaa7c-106">Polecenie cmdlet **Get-AzureRmVMDscExtension** pobiera ustawienia żądanego rozszerzenia konfiguracji stanu (DSC) na konkretnej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eaa7c-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="eaa7c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eaa7c-107">EXAMPLES</span></span>

### <span data-ttu-id="eaa7c-108">Przykład 1: uzyskiwanie ustawień rozszerzenia DSC</span><span class="sxs-lookup"><span data-stu-id="eaa7c-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="eaa7c-109">To polecenie uzyskuje ustawienia dotyczące rozszerzenia o nazwie DSC na maszynie wirtualnej o nazwie VM07.</span><span class="sxs-lookup"><span data-stu-id="eaa7c-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="eaa7c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eaa7c-110">PARAMETERS</span></span>

### <span data-ttu-id="eaa7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa7c-111">-DefaultProfile</span></span>
<span data-ttu-id="eaa7c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eaa7c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaa7c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eaa7c-113">-Name</span></span>
<span data-ttu-id="eaa7c-114">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="eaa7c-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="eaa7c-115">Polecenie cmdlet Set-AzureRmVMDscExtension powoduje ustawienie tej nazwy na Microsoft. PowerShell. DSC, która jest taka sama, jak wartość używana przez polecenie **Get-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="eaa7c-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="eaa7c-116">Ten parametr należy określić tylko w przypadku zmiany nazwy domyślnej w poleceniu cmdlet **Set-AzureRmVMDscExtension** lub użycia innej nazwy zasobu w szablonie Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="eaa7c-116">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="eaa7c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaa7c-117">-ResourceGroupName</span></span>
<span data-ttu-id="eaa7c-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eaa7c-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="eaa7c-119">-Status</span><span class="sxs-lookup"><span data-stu-id="eaa7c-119">-Status</span></span>
<span data-ttu-id="eaa7c-120">Wskazuje, że to polecenie cmdlet pobiera widok wystąpienia rozszerzenia DSC.</span><span class="sxs-lookup"><span data-stu-id="eaa7c-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="eaa7c-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="eaa7c-121">-VMName</span></span>
<span data-ttu-id="eaa7c-122">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="eaa7c-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="eaa7c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa7c-123">CommonParameters</span></span>
<span data-ttu-id="eaa7c-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaa7c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa7c-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaa7c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa7c-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eaa7c-126">INPUTS</span></span>

### <span data-ttu-id="eaa7c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="eaa7c-127">System.String</span></span>

### <span data-ttu-id="eaa7c-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eaa7c-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eaa7c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eaa7c-129">OUTPUTS</span></span>

### <span data-ttu-id="eaa7c-130">Microsoft. Azure. Commands. COMPUTE. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="eaa7c-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="eaa7c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eaa7c-131">NOTES</span></span>

## <span data-ttu-id="eaa7c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eaa7c-132">RELATED LINKS</span></span>

[<span data-ttu-id="eaa7c-133">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="eaa7c-133">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="eaa7c-134">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="eaa7c-134">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


