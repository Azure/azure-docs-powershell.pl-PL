---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
ms.openlocfilehash: 210c66f91836b40c719d91907fc78bd907d0fe86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899382"
---
# <span data-ttu-id="483bc-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="483bc-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="483bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="483bc-102">SYNOPSIS</span></span>
<span data-ttu-id="483bc-103">Pobiera użycie licznika rdzenia maszyny wirtualnej dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="483bc-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="483bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="483bc-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="483bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="483bc-105">DESCRIPTION</span></span>
<span data-ttu-id="483bc-106">Polecenie cmdlet **Get-AzureRmVMUsage** Pobiera liczbę rdzeni maszyny wirtualnej użytkowania dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="483bc-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="483bc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="483bc-107">EXAMPLES</span></span>

### <span data-ttu-id="483bc-108">Przykład 1: pobieranie użycia licznika podstawowego dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="483bc-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="483bc-109">To polecenie uzyskuje użycie licznika rdzenia maszyny wirtualnej dla pozycji Centrala amerykańska.</span><span class="sxs-lookup"><span data-stu-id="483bc-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="483bc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="483bc-110">PARAMETERS</span></span>

### <span data-ttu-id="483bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483bc-111">-DefaultProfile</span></span>
<span data-ttu-id="483bc-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="483bc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="483bc-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="483bc-113">-Location</span></span>
<span data-ttu-id="483bc-114">Określa lokalizację, w której to polecenie cmdlet pobiera użycie licznika rdzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="483bc-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="483bc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483bc-115">CommonParameters</span></span>
<span data-ttu-id="483bc-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483bc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483bc-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="483bc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483bc-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="483bc-118">INPUTS</span></span>

### <span data-ttu-id="483bc-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="483bc-119">None</span></span>
<span data-ttu-id="483bc-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="483bc-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="483bc-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="483bc-121">OUTPUTS</span></span>

### <span data-ttu-id="483bc-122">Microsoft. Azure. Commands. COMPUTE. models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="483bc-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="483bc-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="483bc-123">NOTES</span></span>

## <span data-ttu-id="483bc-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="483bc-124">RELATED LINKS</span></span>

[<span data-ttu-id="483bc-125">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="483bc-125">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


