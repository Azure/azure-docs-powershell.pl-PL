---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: 70f06718c2d96e11b46842e4f39af26d3e29c2f9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893757"
---
# <span data-ttu-id="1f168-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="1f168-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="1f168-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f168-102">SYNOPSIS</span></span>
<span data-ttu-id="1f168-103">Pobiera ustawienia rozszerzenia DSC na określonej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1f168-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="1f168-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f168-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f168-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1f168-105">DESCRIPTION</span></span>
<span data-ttu-id="1f168-106">Polecenie cmdlet **Get-AzVMDscExtension** pobiera ustawienia żądanego rozszerzenia konfiguracji stanu (DSC) na konkretnej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1f168-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="1f168-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f168-107">EXAMPLES</span></span>

### <span data-ttu-id="1f168-108">Przykład 1: uzyskiwanie ustawień rozszerzenia DSC</span><span class="sxs-lookup"><span data-stu-id="1f168-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="1f168-109">To polecenie uzyskuje ustawienia dotyczące rozszerzenia o nazwie DSC na maszynie wirtualnej o nazwie VM07.</span><span class="sxs-lookup"><span data-stu-id="1f168-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="1f168-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f168-110">PARAMETERS</span></span>

### <span data-ttu-id="1f168-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f168-111">-DefaultProfile</span></span>
<span data-ttu-id="1f168-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f168-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f168-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f168-113">-Name</span></span>
<span data-ttu-id="1f168-114">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="1f168-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="1f168-115">Polecenie cmdlet Set-AzVMDscExtension powoduje ustawienie tej nazwy na Microsoft. PowerShell. DSC, która jest taka sama, jak wartość używana przez polecenie **Get-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="1f168-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="1f168-116">Ten parametr należy określić tylko w przypadku zmiany nazwy domyślnej w poleceniu cmdlet **Set-AzVMDscExtension** lub użycia innej nazwy zasobu w szablonie Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="1f168-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="1f168-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f168-117">-ResourceGroupName</span></span>
<span data-ttu-id="1f168-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1f168-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1f168-119">-Status</span><span class="sxs-lookup"><span data-stu-id="1f168-119">-Status</span></span>
<span data-ttu-id="1f168-120">Wskazuje, że to polecenie cmdlet pobiera widok wystąpienia rozszerzenia DSC.</span><span class="sxs-lookup"><span data-stu-id="1f168-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="1f168-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="1f168-121">-VMName</span></span>
<span data-ttu-id="1f168-122">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="1f168-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="1f168-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f168-123">CommonParameters</span></span>
<span data-ttu-id="1f168-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f168-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f168-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f168-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f168-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f168-126">INPUTS</span></span>

### <span data-ttu-id="1f168-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1f168-127">None</span></span>
<span data-ttu-id="1f168-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1f168-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f168-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f168-129">OUTPUTS</span></span>

### <span data-ttu-id="1f168-130">Microsoft. Azure. Commands. COMPUTE. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="1f168-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="1f168-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f168-131">NOTES</span></span>

## <span data-ttu-id="1f168-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f168-132">RELATED LINKS</span></span>

[<span data-ttu-id="1f168-133">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="1f168-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="1f168-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="1f168-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


