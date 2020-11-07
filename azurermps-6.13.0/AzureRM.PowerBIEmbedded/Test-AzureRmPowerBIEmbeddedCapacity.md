---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 306bb6e4e12adcb4a4eda65b2517ddf0648a81fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717380"
---
# <span data-ttu-id="3ef8c-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3ef8c-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3ef8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ef8c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef8c-103">Testowanie istnienia wystąpienia z osadzonymi możliwościami usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="3ef8c-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ef8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ef8c-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ef8c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3ef8c-105">DESCRIPTION</span></span>
<span data-ttu-id="3ef8c-106">Polecenie cmdlet Test-AzureRmPowerBIEmbeddedCapacity testuje istnienie wystąpienia osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="3ef8c-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="3ef8c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ef8c-107">EXAMPLES</span></span>

### <span data-ttu-id="3ef8c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3ef8c-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="3ef8c-109">To polecenie zostanie sprawdzone, jeśli istnieje pojemność o nazwie testcapacity</span><span class="sxs-lookup"><span data-stu-id="3ef8c-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="3ef8c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ef8c-110">PARAMETERS</span></span>

### <span data-ttu-id="3ef8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef8c-111">-DefaultProfile</span></span>
<span data-ttu-id="3ef8c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef8c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ef8c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3ef8c-113">-Name</span></span>
<span data-ttu-id="3ef8c-114">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="3ef8c-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ef8c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef8c-115">CommonParameters</span></span>
<span data-ttu-id="3ef8c-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ef8c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef8c-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ef8c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef8c-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ef8c-118">INPUTS</span></span>

### <span data-ttu-id="3ef8c-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3ef8c-119">None</span></span>

## <span data-ttu-id="3ef8c-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ef8c-120">OUTPUTS</span></span>

### <span data-ttu-id="3ef8c-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ef8c-121">System.Boolean</span></span>

## <span data-ttu-id="3ef8c-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ef8c-122">NOTES</span></span>

## <span data-ttu-id="3ef8c-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ef8c-123">RELATED LINKS</span></span>

[<span data-ttu-id="3ef8c-124">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3ef8c-124">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="3ef8c-125">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3ef8c-125">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
