---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 80fc102c31e4019576a6f2c65ee1c93e19b81590
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872879"
---
# <span data-ttu-id="548c7-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="548c7-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="548c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="548c7-102">SYNOPSIS</span></span>
<span data-ttu-id="548c7-103">Testowanie istnienia wystąpienia z osadzonymi możliwościami usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="548c7-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="548c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="548c7-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="548c7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="548c7-105">DESCRIPTION</span></span>
<span data-ttu-id="548c7-106">Polecenie cmdlet Test-AzPowerBIEmbeddedCapacity testuje istnienie wystąpienia osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="548c7-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="548c7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="548c7-107">EXAMPLES</span></span>

### <span data-ttu-id="548c7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="548c7-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="548c7-109">To polecenie zostanie sprawdzone, jeśli istnieje pojemność o nazwie testcapacity</span><span class="sxs-lookup"><span data-stu-id="548c7-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="548c7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="548c7-110">PARAMETERS</span></span>

### <span data-ttu-id="548c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548c7-111">-DefaultProfile</span></span>
<span data-ttu-id="548c7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="548c7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="548c7-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="548c7-113">-Name</span></span>
<span data-ttu-id="548c7-114">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="548c7-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="548c7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548c7-115">CommonParameters</span></span>
<span data-ttu-id="548c7-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="548c7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548c7-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="548c7-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548c7-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="548c7-118">INPUTS</span></span>

### <span data-ttu-id="548c7-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="548c7-119">None</span></span>

## <span data-ttu-id="548c7-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="548c7-120">OUTPUTS</span></span>

### <span data-ttu-id="548c7-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="548c7-121">System.Boolean</span></span>

## <span data-ttu-id="548c7-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="548c7-122">NOTES</span></span>

## <span data-ttu-id="548c7-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="548c7-123">RELATED LINKS</span></span>

[<span data-ttu-id="548c7-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="548c7-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="548c7-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="548c7-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
