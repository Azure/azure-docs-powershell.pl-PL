---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 5d4f114ef93e0febf7c113f73b8007a9322be752
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718945"
---
# <span data-ttu-id="c82fd-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="c82fd-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="c82fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c82fd-102">SYNOPSIS</span></span>
<span data-ttu-id="c82fd-103">Pobiera użycie licznika rdzenia maszyny wirtualnej dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c82fd-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c82fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c82fd-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [<CommonParameters>]
```

## <span data-ttu-id="c82fd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c82fd-105">DESCRIPTION</span></span>
<span data-ttu-id="c82fd-106">Polecenie cmdlet **Get-AzureRmVMUsage** Pobiera liczbę rdzeni maszyny wirtualnej użytkowania dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c82fd-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="c82fd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c82fd-107">EXAMPLES</span></span>

### <span data-ttu-id="c82fd-108">Przykład 1: pobieranie użycia licznika podstawowego dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="c82fd-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="c82fd-109">To polecenie uzyskuje użycie licznika rdzenia maszyny wirtualnej dla pozycji Centrala amerykańska.</span><span class="sxs-lookup"><span data-stu-id="c82fd-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="c82fd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c82fd-110">PARAMETERS</span></span>

### <span data-ttu-id="c82fd-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c82fd-111">-Location</span></span>
<span data-ttu-id="c82fd-112">Określa lokalizację, w której to polecenie cmdlet pobiera użycie licznika rdzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c82fd-112">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="c82fd-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c82fd-113">CommonParameters</span></span>
<span data-ttu-id="c82fd-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c82fd-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c82fd-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c82fd-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c82fd-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c82fd-116">INPUTS</span></span>

### <span data-ttu-id="c82fd-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c82fd-117">None</span></span>
<span data-ttu-id="c82fd-118">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c82fd-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c82fd-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c82fd-119">OUTPUTS</span></span>

## <span data-ttu-id="c82fd-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c82fd-120">NOTES</span></span>

## <span data-ttu-id="c82fd-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c82fd-121">RELATED LINKS</span></span>

[<span data-ttu-id="c82fd-122">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c82fd-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


