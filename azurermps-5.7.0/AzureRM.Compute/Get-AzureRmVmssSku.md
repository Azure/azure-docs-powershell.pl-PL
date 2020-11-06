---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c86bf549c0de3643aaba67143b7df78f6fce798c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526958"
---
# <span data-ttu-id="b1d64-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="b1d64-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="b1d64-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1d64-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d64-103">Pobiera dostępne jednostki SKU dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="b1d64-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1d64-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1d64-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String> [<CommonParameters>]
```

## <span data-ttu-id="b1d64-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b1d64-105">DESCRIPTION</span></span>
<span data-ttu-id="b1d64-106">Polecenie cmdlet **Get-AzureRmVmssSku** Pobiera dostępne jednostki SKU zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b1d64-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b1d64-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1d64-107">EXAMPLES</span></span>

### <span data-ttu-id="b1d64-108">Przykład 1. Pobierz wszystkie dostępne jednostki SKU z VMSS</span><span class="sxs-lookup"><span data-stu-id="b1d64-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="b1d64-109">To polecenie pobiera wszystkie dostępne jednostki SKU z VMSS o nazwie ContosoVMSS należącej do grupy zasobów o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="b1d64-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="b1d64-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1d64-110">PARAMETERS</span></span>

### <span data-ttu-id="b1d64-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1d64-111">-ResourceGroupName</span></span>
<span data-ttu-id="b1d64-112">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="b1d64-112">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="b1d64-113">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b1d64-113">-VMScaleSetName</span></span>
<span data-ttu-id="b1d64-114">Gatunek nazwy VMSS.</span><span class="sxs-lookup"><span data-stu-id="b1d64-114">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d64-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d64-115">CommonParameters</span></span>
<span data-ttu-id="b1d64-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1d64-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d64-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1d64-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d64-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1d64-118">INPUTS</span></span>

### <span data-ttu-id="b1d64-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b1d64-119">None</span></span>
<span data-ttu-id="b1d64-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b1d64-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1d64-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1d64-121">OUTPUTS</span></span>

### <span data-ttu-id="b1d64-122">To polecenie cmdlet nie produkuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b1d64-122">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="b1d64-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1d64-123">NOTES</span></span>

## <span data-ttu-id="b1d64-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1d64-124">RELATED LINKS</span></span>

[<span data-ttu-id="b1d64-125">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b1d64-125">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


