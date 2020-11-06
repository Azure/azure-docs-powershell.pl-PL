---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1f348a7cddc31a2a3d3d255aa6b4fe80d1808f36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544508"
---
# <span data-ttu-id="dcdc8-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="dcdc8-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="dcdc8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcdc8-102">SYNOPSIS</span></span>
<span data-ttu-id="dcdc8-103">Pobiera informacje o rozszerzeniu skryptu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcdc8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcdc8-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="dcdc8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dcdc8-105">DESCRIPTION</span></span>
<span data-ttu-id="dcdc8-106">Polecenie cmdlet **Get-AzureRmVMCustomScriptExtension** pobiera informacje na temat rozszerzenia maszyny wirtualnej skryptu niestandardowego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="dcdc8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcdc8-107">EXAMPLES</span></span>

### <span data-ttu-id="dcdc8-108">Przykład 1: uzyskiwanie niestandardowego rozszerzenia skryptu</span><span class="sxs-lookup"><span data-stu-id="dcdc8-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="dcdc8-109">To polecenie pobiera niestandardowe rozszerzenie skryptu o nazwie ContosoCustomScript dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="dcdc8-110">Przykład 2: pobieranie widoku wystąpienia niestandardowego rozszerzenia skryptu</span><span class="sxs-lookup"><span data-stu-id="dcdc8-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="dcdc8-111">To polecenie pobiera widok wystąpienia niestandardowego rozszerzenia skryptu o nazwie ContosoCustomScript dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="dcdc8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcdc8-112">PARAMETERS</span></span>

### <span data-ttu-id="dcdc8-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dcdc8-113">-Name</span></span>
<span data-ttu-id="dcdc8-114">Określa nazwę niestandardowego rozszerzenia skryptu, w którym to polecenie cmdlet pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-114">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcdc8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcdc8-115">-ResourceGroupName</span></span>
<span data-ttu-id="dcdc8-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="dcdc8-117">-Status</span><span class="sxs-lookup"><span data-stu-id="dcdc8-117">-Status</span></span>
<span data-ttu-id="dcdc8-118">Wskazuje, że to polecenie cmdlet uzyskuje widok wystąpienia niestandardowego rozszerzenia skryptu.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-118">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcdc8-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="dcdc8-119">-VMName</span></span>
<span data-ttu-id="dcdc8-120">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera niestandardowe rozszerzenie skryptu.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-120">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcdc8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcdc8-121">CommonParameters</span></span>
<span data-ttu-id="dcdc8-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcdc8-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcdc8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcdc8-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcdc8-124">INPUTS</span></span>

### <span data-ttu-id="dcdc8-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dcdc8-125">None</span></span>
<span data-ttu-id="dcdc8-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="dcdc8-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dcdc8-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcdc8-127">OUTPUTS</span></span>

## <span data-ttu-id="dcdc8-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcdc8-128">NOTES</span></span>

## <span data-ttu-id="dcdc8-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcdc8-129">RELATED LINKS</span></span>

[<span data-ttu-id="dcdc8-130">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="dcdc8-130">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="dcdc8-131">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="dcdc8-131">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="dcdc8-132">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="dcdc8-132">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


