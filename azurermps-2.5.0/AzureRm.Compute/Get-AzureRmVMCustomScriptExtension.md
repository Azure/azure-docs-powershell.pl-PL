---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: b6ce3afb8b280b9ca07746979f0bb5ba425afd82
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899386"
---
# <span data-ttu-id="a3615-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a3615-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="a3615-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3615-102">SYNOPSIS</span></span>
<span data-ttu-id="a3615-103">Pobiera informacje o rozszerzeniu skryptu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="a3615-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3615-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3615-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3615-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a3615-105">DESCRIPTION</span></span>
<span data-ttu-id="a3615-106">Polecenie cmdlet **Get-AzureRmVMCustomScriptExtension** pobiera informacje na temat rozszerzenia maszyny wirtualnej skryptu niestandardowego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a3615-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="a3615-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3615-107">EXAMPLES</span></span>

### <span data-ttu-id="a3615-108">Przykład 1: uzyskiwanie niestandardowego rozszerzenia skryptu</span><span class="sxs-lookup"><span data-stu-id="a3615-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="a3615-109">To polecenie pobiera niestandardowe rozszerzenie skryptu o nazwie ContosoCustomScript dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="a3615-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="a3615-110">Przykład 2: pobieranie widoku wystąpienia niestandardowego rozszerzenia skryptu</span><span class="sxs-lookup"><span data-stu-id="a3615-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="a3615-111">To polecenie pobiera widok wystąpienia niestandardowego rozszerzenia skryptu o nazwie ContosoCustomScript dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="a3615-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="a3615-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3615-112">PARAMETERS</span></span>

### <span data-ttu-id="a3615-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3615-113">-DefaultProfile</span></span>
<span data-ttu-id="a3615-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3615-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3615-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3615-115">-Name</span></span>
<span data-ttu-id="a3615-116">Określa nazwę niestandardowego rozszerzenia skryptu, w którym to polecenie cmdlet pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="a3615-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="a3615-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3615-117">-ResourceGroupName</span></span>
<span data-ttu-id="a3615-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a3615-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a3615-119">-Status</span><span class="sxs-lookup"><span data-stu-id="a3615-119">-Status</span></span>
<span data-ttu-id="a3615-120">Wskazuje, że to polecenie cmdlet uzyskuje widok wystąpienia niestandardowego rozszerzenia skryptu.</span><span class="sxs-lookup"><span data-stu-id="a3615-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="a3615-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="a3615-121">-VMName</span></span>
<span data-ttu-id="a3615-122">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera niestandardowe rozszerzenie skryptu.</span><span class="sxs-lookup"><span data-stu-id="a3615-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="a3615-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3615-123">CommonParameters</span></span>
<span data-ttu-id="a3615-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3615-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3615-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3615-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3615-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3615-126">INPUTS</span></span>

### <span data-ttu-id="a3615-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a3615-127">None</span></span>
<span data-ttu-id="a3615-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a3615-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a3615-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3615-129">OUTPUTS</span></span>

### <span data-ttu-id="a3615-130">Microsoft. Azure. Commands. COMPUTE. models. VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="a3615-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="a3615-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3615-131">NOTES</span></span>

## <span data-ttu-id="a3615-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3615-132">RELATED LINKS</span></span>

[<span data-ttu-id="a3615-133">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a3615-133">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="a3615-134">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="a3615-134">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="a3615-135">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="a3615-135">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


