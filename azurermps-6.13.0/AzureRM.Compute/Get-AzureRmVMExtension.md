---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 4aaee403007561797614b2534e29c5918dad3643
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550315"
---
# <span data-ttu-id="3a654-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3a654-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="3a654-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a654-102">SYNOPSIS</span></span>
<span data-ttu-id="3a654-103">Pobiera właściwości rozszerzeń maszyny wirtualnej zainstalowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a654-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a654-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a654-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a654-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a654-105">DESCRIPTION</span></span>
<span data-ttu-id="3a654-106">Polecenie cmdlet **Get-AzureRmVMExtension** pobiera właściwości rozszerzeń maszyny wirtualnej zainstalowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a654-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="3a654-107">Określ nazwę rozszerzenia, dla którego chcesz uzyskać właściwości.</span><span class="sxs-lookup"><span data-stu-id="3a654-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="3a654-108">Aby uzyskać tylko widok wystąpienia rozszerzenia, określ parametr status.</span><span class="sxs-lookup"><span data-stu-id="3a654-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="3a654-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a654-109">EXAMPLES</span></span>

### <span data-ttu-id="3a654-110">Przykład 1: uzyskiwanie właściwości rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="3a654-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="3a654-111">To polecenie pobiera właściwości rozszerzenia o nazwie CustomScriptExtension na maszynie wirtualnej o nazwie VirtualMachine22 w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3a654-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="3a654-112">Przykład 2: pobieranie widoku wystąpienia rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="3a654-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="3a654-113">To polecenie uzyskuje widok wystąpienia dla rozszerzenia o nazwie CustomScriptExtension na maszynie wirtualnej o nazwie VirtualMachine22 w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3a654-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="3a654-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a654-114">PARAMETERS</span></span>

### <span data-ttu-id="3a654-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a654-115">-DefaultProfile</span></span>
<span data-ttu-id="3a654-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a654-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a654-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a654-117">-Name</span></span>
<span data-ttu-id="3a654-118">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="3a654-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="3a654-119">To polecenie cmdlet umożliwia pobieranie właściwości rozszerzenia, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3a654-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a654-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a654-120">-ResourceGroupName</span></span>
<span data-ttu-id="3a654-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a654-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3a654-122">-Status</span><span class="sxs-lookup"><span data-stu-id="3a654-122">-Status</span></span>
<span data-ttu-id="3a654-123">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="3a654-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="3a654-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="3a654-124">-VMName</span></span>
<span data-ttu-id="3a654-125">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a654-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3a654-126">To polecenie cmdlet pobiera właściwości rozszerzenia z maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="3a654-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3a654-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a654-127">CommonParameters</span></span>
<span data-ttu-id="3a654-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a654-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a654-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a654-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a654-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a654-130">INPUTS</span></span>

### <span data-ttu-id="3a654-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3a654-131">System.String</span></span>

### <span data-ttu-id="3a654-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3a654-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3a654-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a654-133">OUTPUTS</span></span>

### <span data-ttu-id="3a654-134">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="3a654-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="3a654-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a654-135">NOTES</span></span>

## <span data-ttu-id="3a654-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a654-136">RELATED LINKS</span></span>

[<span data-ttu-id="3a654-137">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3a654-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="3a654-138">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3a654-138">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


