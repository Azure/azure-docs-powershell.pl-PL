---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: a8ac31efd77d5b8ff5c07920bb14b44f80ac0955
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893754"
---
# <span data-ttu-id="53f6c-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="53f6c-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="53f6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="53f6c-103">Pobiera właściwości rozszerzeń maszyny wirtualnej zainstalowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="53f6c-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="53f6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53f6c-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53f6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="53f6c-105">DESCRIPTION</span></span>
<span data-ttu-id="53f6c-106">Polecenie cmdlet **Get-AzVMExtension** pobiera właściwości rozszerzeń maszyny wirtualnej zainstalowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="53f6c-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="53f6c-107">Określ nazwę rozszerzenia, dla którego chcesz uzyskać właściwości.</span><span class="sxs-lookup"><span data-stu-id="53f6c-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="53f6c-108">Aby uzyskać tylko widok wystąpienia rozszerzenia, określ parametr status.</span><span class="sxs-lookup"><span data-stu-id="53f6c-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="53f6c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53f6c-109">EXAMPLES</span></span>

### <span data-ttu-id="53f6c-110">Przykład 1: uzyskiwanie właściwości rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="53f6c-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="53f6c-111">To polecenie pobiera właściwości rozszerzenia o nazwie CustomScriptExtension na maszynie wirtualnej o nazwie VirtualMachine22 w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="53f6c-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="53f6c-112">Przykład 2: pobieranie widoku wystąpienia rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="53f6c-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="53f6c-113">To polecenie uzyskuje widok wystąpienia dla rozszerzenia o nazwie CustomScriptExtension na maszynie wirtualnej o nazwie VirtualMachine22 w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="53f6c-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="53f6c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53f6c-114">PARAMETERS</span></span>

### <span data-ttu-id="53f6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f6c-115">-DefaultProfile</span></span>
<span data-ttu-id="53f6c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53f6c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53f6c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53f6c-117">-Name</span></span>
<span data-ttu-id="53f6c-118">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="53f6c-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="53f6c-119">To polecenie cmdlet umożliwia pobieranie właściwości rozszerzenia, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="53f6c-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="53f6c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f6c-120">-ResourceGroupName</span></span>
<span data-ttu-id="53f6c-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="53f6c-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="53f6c-122">-Status</span><span class="sxs-lookup"><span data-stu-id="53f6c-122">-Status</span></span>
<span data-ttu-id="53f6c-123">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="53f6c-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="53f6c-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="53f6c-124">-VMName</span></span>
<span data-ttu-id="53f6c-125">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="53f6c-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="53f6c-126">To polecenie cmdlet pobiera właściwości rozszerzenia z maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="53f6c-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="53f6c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f6c-127">CommonParameters</span></span>
<span data-ttu-id="53f6c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f6c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f6c-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53f6c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f6c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53f6c-130">INPUTS</span></span>

### <span data-ttu-id="53f6c-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="53f6c-131">None</span></span>
<span data-ttu-id="53f6c-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="53f6c-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="53f6c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53f6c-133">OUTPUTS</span></span>

### <span data-ttu-id="53f6c-134">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="53f6c-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="53f6c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53f6c-135">NOTES</span></span>

## <span data-ttu-id="53f6c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53f6c-136">RELATED LINKS</span></span>

[<span data-ttu-id="53f6c-137">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="53f6c-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="53f6c-138">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="53f6c-138">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


