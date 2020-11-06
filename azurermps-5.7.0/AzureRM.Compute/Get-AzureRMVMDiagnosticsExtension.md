---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: 32d3d5a152f36c0e4e5f8e3e4e4ecc2b8eb6ee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545791"
---
# <span data-ttu-id="616cd-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="616cd-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="616cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="616cd-102">SYNOPSIS</span></span>
<span data-ttu-id="616cd-103">Pobiera ustawienia rozszerzenia diagnostycznego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616cd-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="616cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="616cd-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="616cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="616cd-105">DESCRIPTION</span></span>
<span data-ttu-id="616cd-106">Polecenie cmdlet **Get-AzureRmVMDiagnosticsExtension** pobiera ustawienia rozszerzenia Diagnostyka platformy Azure na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616cd-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="616cd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="616cd-107">EXAMPLES</span></span>

### <span data-ttu-id="616cd-108">Przykład 1: uzyskiwanie rozszerzenia diagnostycznego zastosowanego do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="616cd-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="616cd-109">To polecenie powoduje wyświetlenie rozszerzenia diagnostycznego zastosowanego do maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="616cd-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="616cd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="616cd-110">PARAMETERS</span></span>

### <span data-ttu-id="616cd-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="616cd-111">-Name</span></span>
<span data-ttu-id="616cd-112">Określa nazwę rozszerzenia diagnostycznego, dla którego to polecenie cmdlet pobiera ustawienia.</span><span class="sxs-lookup"><span data-stu-id="616cd-112">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616cd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="616cd-113">-ResourceGroupName</span></span>
<span data-ttu-id="616cd-114">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616cd-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="616cd-115">-Status</span><span class="sxs-lookup"><span data-stu-id="616cd-115">-Status</span></span>
<span data-ttu-id="616cd-116">Wskazuje, że w tym poleceniu cmdlet jest używana wartość stanu.</span><span class="sxs-lookup"><span data-stu-id="616cd-116">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="616cd-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="616cd-117">-VMName</span></span>
<span data-ttu-id="616cd-118">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet uzyskuje rozszerzenie diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="616cd-118">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="616cd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="616cd-119">CommonParameters</span></span>
<span data-ttu-id="616cd-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="616cd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="616cd-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="616cd-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="616cd-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="616cd-122">INPUTS</span></span>

### <span data-ttu-id="616cd-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="616cd-123">None</span></span>
<span data-ttu-id="616cd-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="616cd-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="616cd-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="616cd-125">OUTPUTS</span></span>

## <span data-ttu-id="616cd-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="616cd-126">NOTES</span></span>

## <span data-ttu-id="616cd-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="616cd-127">RELATED LINKS</span></span>

[<span data-ttu-id="616cd-128">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="616cd-128">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="616cd-129">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="616cd-129">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


