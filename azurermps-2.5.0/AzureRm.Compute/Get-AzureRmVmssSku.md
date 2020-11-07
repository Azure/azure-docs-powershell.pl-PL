---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsssku
schema: 2.0.0
ms.openlocfilehash: 307b9852f506368e1e13c02fac4532dab4d2ddd2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898803"
---
# <span data-ttu-id="56052-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="56052-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="56052-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56052-102">SYNOPSIS</span></span>
<span data-ttu-id="56052-103">Pobiera dostępne jednostki SKU dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="56052-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56052-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56052-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56052-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56052-105">DESCRIPTION</span></span>
<span data-ttu-id="56052-106">Polecenie cmdlet **Get-AzureRmVmssSku** Pobiera dostępne jednostki SKU zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="56052-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="56052-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56052-107">EXAMPLES</span></span>

### <span data-ttu-id="56052-108">Przykład 1. Pobierz wszystkie dostępne jednostki SKU z VMSS</span><span class="sxs-lookup"><span data-stu-id="56052-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="56052-109">To polecenie pobiera wszystkie dostępne jednostki SKU z VMSS o nazwie ContosoVMSS należącej do grupy zasobów o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="56052-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="56052-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56052-110">PARAMETERS</span></span>

### <span data-ttu-id="56052-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56052-111">-DefaultProfile</span></span>
<span data-ttu-id="56052-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56052-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56052-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56052-113">-ResourceGroupName</span></span>
<span data-ttu-id="56052-114">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="56052-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="56052-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="56052-115">-VMScaleSetName</span></span>
<span data-ttu-id="56052-116">Gatunek nazwy VMSS.</span><span class="sxs-lookup"><span data-stu-id="56052-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="56052-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56052-117">CommonParameters</span></span>
<span data-ttu-id="56052-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56052-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56052-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56052-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56052-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56052-120">INPUTS</span></span>

### <span data-ttu-id="56052-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="56052-121">None</span></span>
<span data-ttu-id="56052-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="56052-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56052-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56052-123">OUTPUTS</span></span>

### <span data-ttu-id="56052-124">To polecenie cmdlet nie produkuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="56052-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="56052-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56052-125">NOTES</span></span>

## <span data-ttu-id="56052-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56052-126">RELATED LINKS</span></span>

[<span data-ttu-id="56052-127">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56052-127">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


