---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 9e7cb85bf29d6982271768af6948db1d3c5b8605
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542719"
---
# <span data-ttu-id="a8bfb-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a8bfb-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="a8bfb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="a8bfb-103">Pobiera informacje o rozszerzeniu VMAccess.</span><span class="sxs-lookup"><span data-stu-id="a8bfb-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8bfb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8bfb-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="a8bfb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a8bfb-105">DESCRIPTION</span></span>
<span data-ttu-id="a8bfb-106">Polecenie cmdlet **Get-AzureRmVMAccessExtension** pobiera informacje o rozszerzeniu maszyny wirtualnej dostępu do maszyny wirtualnej (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="a8bfb-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="a8bfb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8bfb-107">EXAMPLES</span></span>

### <span data-ttu-id="a8bfb-108">Przykład 1: uzyskiwanie rozszerzenia VMAccess</span><span class="sxs-lookup"><span data-stu-id="a8bfb-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="a8bfb-109">To polecenie uzyskuje rozszerzenie VMAccess o nazwie ContosoTest dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="a8bfb-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="a8bfb-110">Przykład 2: uzyskiwanie widoku wystąpienia rozszerzenia VMAccess</span><span class="sxs-lookup"><span data-stu-id="a8bfb-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="a8bfb-111">To polecenie pobiera widok wystąpienia rozszerzenia VMAccess o nazwie ContosoTest dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="a8bfb-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="a8bfb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8bfb-112">PARAMETERS</span></span>

### <span data-ttu-id="a8bfb-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a8bfb-113">-Name</span></span>
<span data-ttu-id="a8bfb-114">Określa nazwę rozszerzenia, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8bfb-114">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a8bfb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8bfb-115">-ResourceGroupName</span></span>
<span data-ttu-id="a8bfb-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a8bfb-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a8bfb-117">-Status</span><span class="sxs-lookup"><span data-stu-id="a8bfb-117">-Status</span></span>
<span data-ttu-id="a8bfb-118">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="a8bfb-118">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="a8bfb-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="a8bfb-119">-VMName</span></span>
<span data-ttu-id="a8bfb-120">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a8bfb-120">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a8bfb-121">To polecenie cmdlet umożliwia pobieranie informacji o VMAccess dla maszyny wirtualnej określanej przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a8bfb-121">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="a8bfb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8bfb-122">CommonParameters</span></span>
<span data-ttu-id="a8bfb-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8bfb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8bfb-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8bfb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8bfb-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8bfb-125">INPUTS</span></span>

### <span data-ttu-id="a8bfb-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a8bfb-126">None</span></span>
<span data-ttu-id="a8bfb-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a8bfb-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8bfb-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8bfb-128">OUTPUTS</span></span>

## <span data-ttu-id="a8bfb-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8bfb-129">NOTES</span></span>

## <span data-ttu-id="a8bfb-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8bfb-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8bfb-131">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a8bfb-131">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="a8bfb-132">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a8bfb-132">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="a8bfb-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="a8bfb-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


