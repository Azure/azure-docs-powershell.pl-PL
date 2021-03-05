---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 0b7d1f72b25da91e85a578a88eded7a511d6d1fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996087"
---
# <span data-ttu-id="99634-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="99634-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="99634-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99634-102">SYNOPSIS</span></span>
<span data-ttu-id="99634-103">Sprawdza istnienie wystąpienia osadzonej pojemności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="99634-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="99634-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99634-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99634-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="99634-105">DESCRIPTION</span></span>
<span data-ttu-id="99634-106">Polecenie Test-AzPowerBIEmbeddedCapacity cmdlet sprawdza istnienie wystąpienia osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="99634-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="99634-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99634-107">EXAMPLES</span></span>

### <span data-ttu-id="99634-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99634-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="99634-109">To polecenie sprawdzi, czy istnieje pojemność o nazwie testcapacity</span><span class="sxs-lookup"><span data-stu-id="99634-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="99634-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99634-110">PARAMETERS</span></span>

### <span data-ttu-id="99634-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99634-111">-DefaultProfile</span></span>
<span data-ttu-id="99634-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="99634-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99634-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="99634-113">-Name</span></span>
<span data-ttu-id="99634-114">Nazwa osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="99634-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="99634-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99634-115">CommonParameters</span></span>
<span data-ttu-id="99634-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99634-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99634-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99634-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99634-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99634-118">INPUTS</span></span>

### <span data-ttu-id="99634-119">Brak</span><span class="sxs-lookup"><span data-stu-id="99634-119">None</span></span>

## <span data-ttu-id="99634-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99634-120">OUTPUTS</span></span>

### <span data-ttu-id="99634-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="99634-121">System.Boolean</span></span>

## <span data-ttu-id="99634-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99634-122">NOTES</span></span>

## <span data-ttu-id="99634-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99634-123">RELATED LINKS</span></span>

[<span data-ttu-id="99634-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="99634-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="99634-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="99634-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
