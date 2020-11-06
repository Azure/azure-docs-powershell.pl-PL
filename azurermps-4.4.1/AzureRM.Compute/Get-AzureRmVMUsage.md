---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: af360334ab546685deadad45c2ea3f8954c226f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550036"
---
# <span data-ttu-id="88d9d-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="88d9d-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="88d9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="88d9d-103">Pobiera użycie licznika rdzenia maszyny wirtualnej dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="88d9d-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88d9d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88d9d-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88d9d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88d9d-105">DESCRIPTION</span></span>
<span data-ttu-id="88d9d-106">Polecenie cmdlet **Get-AzureRmVMUsage** Pobiera liczbę rdzeni maszyny wirtualnej użytkowania dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="88d9d-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="88d9d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88d9d-107">EXAMPLES</span></span>

### <span data-ttu-id="88d9d-108">Przykład 1: pobieranie użycia licznika podstawowego dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="88d9d-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="88d9d-109">To polecenie uzyskuje użycie licznika rdzenia maszyny wirtualnej dla pozycji Centrala amerykańska.</span><span class="sxs-lookup"><span data-stu-id="88d9d-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="88d9d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88d9d-110">PARAMETERS</span></span>

### <span data-ttu-id="88d9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88d9d-111">-DefaultProfile</span></span>
<span data-ttu-id="88d9d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88d9d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88d9d-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="88d9d-113">-Location</span></span>
<span data-ttu-id="88d9d-114">Określa lokalizację, w której to polecenie cmdlet pobiera użycie licznika rdzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="88d9d-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="88d9d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d9d-115">CommonParameters</span></span>
<span data-ttu-id="88d9d-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88d9d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d9d-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88d9d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d9d-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88d9d-118">INPUTS</span></span>

## <span data-ttu-id="88d9d-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88d9d-119">OUTPUTS</span></span>

## <span data-ttu-id="88d9d-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88d9d-120">NOTES</span></span>

## <span data-ttu-id="88d9d-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88d9d-121">RELATED LINKS</span></span>

[<span data-ttu-id="88d9d-122">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88d9d-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


