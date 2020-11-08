---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049299"
---
# <span data-ttu-id="f4d7d-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f4d7d-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f4d7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4d7d-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d7d-103">Testowanie istnienia wystąpienia z osadzonymi możliwościami usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="f4d7d-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="f4d7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4d7d-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4d7d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f4d7d-105">DESCRIPTION</span></span>
<span data-ttu-id="f4d7d-106">Polecenie cmdlet Test-AzPowerBIEmbeddedCapacity testuje istnienie wystąpienia osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="f4d7d-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="f4d7d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4d7d-107">EXAMPLES</span></span>

### <span data-ttu-id="f4d7d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f4d7d-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="f4d7d-109">To polecenie zostanie sprawdzone, jeśli istnieje pojemność o nazwie testcapacity</span><span class="sxs-lookup"><span data-stu-id="f4d7d-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="f4d7d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4d7d-110">PARAMETERS</span></span>

### <span data-ttu-id="f4d7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d7d-111">-DefaultProfile</span></span>
<span data-ttu-id="f4d7d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d7d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4d7d-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f4d7d-113">-Name</span></span>
<span data-ttu-id="f4d7d-114">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="f4d7d-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="f4d7d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d7d-115">CommonParameters</span></span>
<span data-ttu-id="f4d7d-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d7d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d7d-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4d7d-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d7d-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4d7d-118">INPUTS</span></span>

### <span data-ttu-id="f4d7d-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f4d7d-119">None</span></span>

## <span data-ttu-id="f4d7d-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4d7d-120">OUTPUTS</span></span>

### <span data-ttu-id="f4d7d-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4d7d-121">System.Boolean</span></span>

## <span data-ttu-id="f4d7d-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4d7d-122">NOTES</span></span>

## <span data-ttu-id="f4d7d-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4d7d-123">RELATED LINKS</span></span>

[<span data-ttu-id="f4d7d-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f4d7d-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="f4d7d-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f4d7d-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
