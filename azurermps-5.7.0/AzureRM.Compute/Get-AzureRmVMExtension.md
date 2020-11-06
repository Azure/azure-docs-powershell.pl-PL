---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 82ab2f02d47b17342f71b09eebe826fc48c07b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526977"
---
# <span data-ttu-id="d00d3-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="d00d3-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="d00d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d00d3-102">SYNOPSIS</span></span>
<span data-ttu-id="d00d3-103">Pobiera właściwości rozszerzeń maszyny wirtualnej zainstalowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d00d3-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d00d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d00d3-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="d00d3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d00d3-105">DESCRIPTION</span></span>
<span data-ttu-id="d00d3-106">Polecenie cmdlet **Get-AzureRmVMExtension** pobiera właściwości rozszerzeń maszyny wirtualnej zainstalowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d00d3-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="d00d3-107">Określ nazwę rozszerzenia, dla którego chcesz uzyskać właściwości.</span><span class="sxs-lookup"><span data-stu-id="d00d3-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="d00d3-108">Aby uzyskać tylko widok wystąpienia rozszerzenia, określ parametr status.</span><span class="sxs-lookup"><span data-stu-id="d00d3-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="d00d3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d00d3-109">EXAMPLES</span></span>

### <span data-ttu-id="d00d3-110">Przykład 1: uzyskiwanie właściwości rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="d00d3-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="d00d3-111">To polecenie pobiera właściwości rozszerzenia o nazwie CustomScriptExtension na maszynie wirtualnej o nazwie VirtualMachine22 w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d00d3-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="d00d3-112">Przykład 2: pobieranie widoku wystąpienia rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="d00d3-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="d00d3-113">To polecenie uzyskuje widok wystąpienia dla rozszerzenia o nazwie CustomScriptExtension na maszynie wirtualnej o nazwie VirtualMachine22 w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d00d3-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="d00d3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d00d3-114">PARAMETERS</span></span>

### <span data-ttu-id="d00d3-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d00d3-115">-Name</span></span>
<span data-ttu-id="d00d3-116">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d00d3-116">Specifies the name of an extension.</span></span>
<span data-ttu-id="d00d3-117">To polecenie cmdlet umożliwia pobieranie właściwości rozszerzenia, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d00d3-117">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="d00d3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d00d3-118">-ResourceGroupName</span></span>
<span data-ttu-id="d00d3-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d00d3-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d00d3-120">-Status</span><span class="sxs-lookup"><span data-stu-id="d00d3-120">-Status</span></span>
<span data-ttu-id="d00d3-121">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d00d3-121">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="d00d3-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="d00d3-122">-VMName</span></span>
<span data-ttu-id="d00d3-123">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d00d3-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d00d3-124">To polecenie cmdlet pobiera właściwości rozszerzenia z maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d00d3-124">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d00d3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d00d3-125">CommonParameters</span></span>
<span data-ttu-id="d00d3-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d00d3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d00d3-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d00d3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d00d3-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d00d3-128">INPUTS</span></span>

### <span data-ttu-id="d00d3-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d00d3-129">None</span></span>
<span data-ttu-id="d00d3-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d00d3-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d00d3-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d00d3-131">OUTPUTS</span></span>

## <span data-ttu-id="d00d3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d00d3-132">NOTES</span></span>

## <span data-ttu-id="d00d3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d00d3-133">RELATED LINKS</span></span>

[<span data-ttu-id="d00d3-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="d00d3-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="d00d3-135">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="d00d3-135">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


