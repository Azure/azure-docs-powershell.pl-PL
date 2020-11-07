---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 0996b327a0253e5f20c693fb8a3f3229597c80e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710299"
---
# <span data-ttu-id="59131-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="59131-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="59131-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59131-102">SYNOPSIS</span></span>
<span data-ttu-id="59131-103">Pobiera użycie licznika rdzenia maszyny wirtualnej dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="59131-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="59131-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59131-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59131-105">Opis</span><span class="sxs-lookup"><span data-stu-id="59131-105">DESCRIPTION</span></span>
<span data-ttu-id="59131-106">Polecenie cmdlet **Get-AzVMUsage** Pobiera liczbę rdzeni maszyny wirtualnej użytkowania dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="59131-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="59131-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59131-107">EXAMPLES</span></span>

### <span data-ttu-id="59131-108">Przykład 1: pobieranie użycia licznika podstawowego dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="59131-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="59131-109">To polecenie uzyskuje użycie licznika rdzenia maszyny wirtualnej dla pozycji Centrala amerykańska.</span><span class="sxs-lookup"><span data-stu-id="59131-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="59131-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59131-110">PARAMETERS</span></span>

### <span data-ttu-id="59131-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59131-111">-DefaultProfile</span></span>
<span data-ttu-id="59131-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="59131-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59131-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="59131-113">-Location</span></span>
<span data-ttu-id="59131-114">Określa lokalizację, w której to polecenie cmdlet pobiera użycie licznika rdzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="59131-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="59131-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59131-115">CommonParameters</span></span>
<span data-ttu-id="59131-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59131-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59131-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59131-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59131-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59131-118">INPUTS</span></span>

### <span data-ttu-id="59131-119">System. String</span><span class="sxs-lookup"><span data-stu-id="59131-119">System.String</span></span>

## <span data-ttu-id="59131-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59131-120">OUTPUTS</span></span>

### <span data-ttu-id="59131-121">Microsoft. Azure. Commands. COMPUTE. models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="59131-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="59131-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59131-122">NOTES</span></span>

## <span data-ttu-id="59131-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59131-123">RELATED LINKS</span></span>

[<span data-ttu-id="59131-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="59131-124">Get-AzVM</span></span>](./Get-AzVM.md)


