---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: d005f3f182109399f5a74b934959951dfb02c48e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893705"
---
# <span data-ttu-id="caca2-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="caca2-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="caca2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="caca2-102">SYNOPSIS</span></span>
<span data-ttu-id="caca2-103">Pobiera dostępne jednostki SKU dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="caca2-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="caca2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="caca2-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caca2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="caca2-105">DESCRIPTION</span></span>
<span data-ttu-id="caca2-106">Polecenie cmdlet **Get-AzVmssSku** Pobiera dostępne jednostki SKU zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="caca2-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="caca2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="caca2-107">EXAMPLES</span></span>

### <span data-ttu-id="caca2-108">Przykład 1. Pobierz wszystkie dostępne jednostki SKU z VMSS</span><span class="sxs-lookup"><span data-stu-id="caca2-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="caca2-109">To polecenie pobiera wszystkie dostępne jednostki SKU z VMSS o nazwie ContosoVMSS należącej do grupy zasobów o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="caca2-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="caca2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="caca2-110">PARAMETERS</span></span>

### <span data-ttu-id="caca2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caca2-111">-DefaultProfile</span></span>
<span data-ttu-id="caca2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="caca2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caca2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caca2-113">-ResourceGroupName</span></span>
<span data-ttu-id="caca2-114">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="caca2-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="caca2-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="caca2-115">-VMScaleSetName</span></span>
<span data-ttu-id="caca2-116">Gatunek nazwy VMSS.</span><span class="sxs-lookup"><span data-stu-id="caca2-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="caca2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caca2-117">CommonParameters</span></span>
<span data-ttu-id="caca2-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caca2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caca2-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caca2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caca2-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="caca2-120">INPUTS</span></span>

### <span data-ttu-id="caca2-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="caca2-121">None</span></span>
<span data-ttu-id="caca2-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="caca2-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="caca2-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="caca2-123">OUTPUTS</span></span>

### <span data-ttu-id="caca2-124">To polecenie cmdlet nie produkuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="caca2-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="caca2-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="caca2-125">NOTES</span></span>

## <span data-ttu-id="caca2-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="caca2-126">RELATED LINKS</span></span>

[<span data-ttu-id="caca2-127">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="caca2-127">Get-AzVmss</span></span>](./Get-AzVmss.md)


