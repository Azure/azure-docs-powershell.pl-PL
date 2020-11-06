---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
ms.openlocfilehash: 0a3c54331b557b6be279ab5ce3f9fafad62b158c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526985"
---
# <span data-ttu-id="acaa0-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="acaa0-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="acaa0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="acaa0-102">SYNOPSIS</span></span>
<span data-ttu-id="acaa0-103">Pobiera ustawienia rozszerzenia DSC na określonej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="acaa0-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acaa0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="acaa0-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="acaa0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="acaa0-105">DESCRIPTION</span></span>
<span data-ttu-id="acaa0-106">Polecenie cmdlet **Get-AzureRmVMDscExtension** pobiera ustawienia żądanego rozszerzenia konfiguracji stanu (DSC) na konkretnej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="acaa0-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="acaa0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="acaa0-107">EXAMPLES</span></span>

### <span data-ttu-id="acaa0-108">Przykład 1: uzyskiwanie ustawień rozszerzenia DSC</span><span class="sxs-lookup"><span data-stu-id="acaa0-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="acaa0-109">To polecenie uzyskuje ustawienia dotyczące rozszerzenia o nazwie DSC na maszynie wirtualnej o nazwie VM07.</span><span class="sxs-lookup"><span data-stu-id="acaa0-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="acaa0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="acaa0-110">PARAMETERS</span></span>

### <span data-ttu-id="acaa0-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="acaa0-111">-Name</span></span>
<span data-ttu-id="acaa0-112">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="acaa0-112">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="acaa0-113">Polecenie cmdlet Set-AzureRmVMDscExtension powoduje ustawienie tej nazwy na Microsoft. PowerShell. DSC, która jest taka sama, jak wartość używana przez polecenie **Get-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="acaa0-113">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="acaa0-114">Ten parametr należy określić tylko w przypadku zmiany nazwy domyślnej w poleceniu cmdlet **Set-AzureRmVMDscExtension** lub użycia innej nazwy zasobu w szablonie Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="acaa0-114">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acaa0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acaa0-115">-ResourceGroupName</span></span>
<span data-ttu-id="acaa0-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="acaa0-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acaa0-117">-Status</span><span class="sxs-lookup"><span data-stu-id="acaa0-117">-Status</span></span>
<span data-ttu-id="acaa0-118">Wskazuje, że to polecenie cmdlet pobiera widok wystąpienia rozszerzenia DSC.</span><span class="sxs-lookup"><span data-stu-id="acaa0-118">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acaa0-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="acaa0-119">-VMName</span></span>
<span data-ttu-id="acaa0-120">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="acaa0-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="acaa0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acaa0-121">CommonParameters</span></span>
<span data-ttu-id="acaa0-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acaa0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acaa0-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acaa0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acaa0-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="acaa0-124">INPUTS</span></span>

### <span data-ttu-id="acaa0-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="acaa0-125">None</span></span>
<span data-ttu-id="acaa0-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="acaa0-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="acaa0-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="acaa0-127">OUTPUTS</span></span>

### <span data-ttu-id="acaa0-128">Microsoft. Azure. Commands. COMPUTE. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="acaa0-128">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="acaa0-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="acaa0-129">NOTES</span></span>

## <span data-ttu-id="acaa0-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="acaa0-130">RELATED LINKS</span></span>

[<span data-ttu-id="acaa0-131">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="acaa0-131">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="acaa0-132">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="acaa0-132">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


