---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8f6e161ad9ae2078da15dda659f1aea13929eec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525045"
---
# <span data-ttu-id="51e69-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="51e69-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="51e69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51e69-102">SYNOPSIS</span></span>
<span data-ttu-id="51e69-103">Testowanie istnienia wystąpienia z osadzonymi możliwościami usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="51e69-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51e69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51e69-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="51e69-105">Opis</span><span class="sxs-lookup"><span data-stu-id="51e69-105">DESCRIPTION</span></span>
<span data-ttu-id="51e69-106">Polecenie cmdlet Test-AzureRmPowerBIEmbeddedCapacity testuje istnienie wystąpienia osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="51e69-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="51e69-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51e69-107">EXAMPLES</span></span>

### <span data-ttu-id="51e69-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51e69-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="51e69-109">To polecenie zostanie sprawdzone, jeśli istnieje pojemność o nazwie testcapacity</span><span class="sxs-lookup"><span data-stu-id="51e69-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="51e69-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51e69-110">PARAMETERS</span></span>

### <span data-ttu-id="51e69-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51e69-111">-Name</span></span>
<span data-ttu-id="51e69-112">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="51e69-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="51e69-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e69-113">CommonParameters</span></span>
<span data-ttu-id="51e69-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51e69-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e69-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51e69-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e69-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51e69-116">INPUTS</span></span>

### <span data-ttu-id="51e69-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="51e69-117">None</span></span>
<span data-ttu-id="51e69-118">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="51e69-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="51e69-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51e69-119">OUTPUTS</span></span>

### <span data-ttu-id="51e69-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51e69-120">System.Boolean</span></span>

## <span data-ttu-id="51e69-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51e69-121">NOTES</span></span>

## <span data-ttu-id="51e69-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51e69-122">RELATED LINKS</span></span>

[<span data-ttu-id="51e69-123">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="51e69-123">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="51e69-124">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="51e69-124">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
