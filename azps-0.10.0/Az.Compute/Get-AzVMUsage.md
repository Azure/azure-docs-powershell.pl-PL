---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 66a74ed2fa389c0dd39fa9fc86570ff8d68dc1dc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893709"
---
# <span data-ttu-id="e91e5-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="e91e5-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="e91e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e91e5-102">SYNOPSIS</span></span>
<span data-ttu-id="e91e5-103">Pobiera użycie licznika rdzenia maszyny wirtualnej dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="e91e5-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="e91e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e91e5-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e91e5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e91e5-105">DESCRIPTION</span></span>
<span data-ttu-id="e91e5-106">Polecenie cmdlet **Get-AzVMUsage** Pobiera liczbę rdzeni maszyny wirtualnej użytkowania dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="e91e5-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="e91e5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e91e5-107">EXAMPLES</span></span>

### <span data-ttu-id="e91e5-108">Przykład 1: pobieranie użycia licznika podstawowego dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="e91e5-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="e91e5-109">To polecenie uzyskuje użycie licznika rdzenia maszyny wirtualnej dla pozycji Centrala amerykańska.</span><span class="sxs-lookup"><span data-stu-id="e91e5-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="e91e5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e91e5-110">PARAMETERS</span></span>

### <span data-ttu-id="e91e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e91e5-111">-DefaultProfile</span></span>
<span data-ttu-id="e91e5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e91e5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e91e5-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e91e5-113">-Location</span></span>
<span data-ttu-id="e91e5-114">Określa lokalizację, w której to polecenie cmdlet pobiera użycie licznika rdzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e91e5-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="e91e5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e91e5-115">CommonParameters</span></span>
<span data-ttu-id="e91e5-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e91e5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e91e5-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e91e5-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e91e5-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e91e5-118">INPUTS</span></span>

### <span data-ttu-id="e91e5-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e91e5-119">None</span></span>
<span data-ttu-id="e91e5-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e91e5-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e91e5-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e91e5-121">OUTPUTS</span></span>

### <span data-ttu-id="e91e5-122">Microsoft. Azure. Commands. COMPUTE. models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="e91e5-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="e91e5-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e91e5-123">NOTES</span></span>

## <span data-ttu-id="e91e5-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e91e5-124">RELATED LINKS</span></span>

[<span data-ttu-id="e91e5-125">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e91e5-125">Get-AzVM</span></span>](./Get-AzVM.md)


