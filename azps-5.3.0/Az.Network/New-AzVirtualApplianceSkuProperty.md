---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385380"
---
# <span data-ttu-id="38894-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="38894-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="38894-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38894-102">SYNOPSIS</span></span>
<span data-ttu-id="38894-103">Zdefiniuj dla zasobu jednostkę SKU sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="38894-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="38894-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38894-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38894-105">Opis</span><span class="sxs-lookup"><span data-stu-id="38894-105">DESCRIPTION</span></span>
<span data-ttu-id="38894-106">Polecenie New-AzVirtualApplianceSkuProperties definiuje jednostkę SKU dla zasobu sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="38894-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="38894-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38894-107">EXAMPLES</span></span>

### <span data-ttu-id="38894-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="38894-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="38894-109">Utwórz obiekt właściwości jednostki SKU urządzenia wirtualnego, który ma być wykorzystywany z poleceniem New-AzNetworkVirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="38894-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="38894-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38894-110">PARAMETERS</span></span>

### <span data-ttu-id="38894-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="38894-111">-BundledScaleUnit</span></span>
<span data-ttu-id="38894-112">Pakietowa jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="38894-112">The bundled scale unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38894-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38894-113">-DefaultProfile</span></span>
<span data-ttu-id="38894-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38894-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38894-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="38894-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="38894-116">Wersja na rynku.</span><span class="sxs-lookup"><span data-stu-id="38894-116">The market place version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38894-117">-NazwaDostawcy</span><span class="sxs-lookup"><span data-stu-id="38894-117">-VendorName</span></span>
<span data-ttu-id="38894-118">Nazwa dostawcy.</span><span class="sxs-lookup"><span data-stu-id="38894-118">The name of the vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38894-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38894-119">CommonParameters</span></span>
<span data-ttu-id="38894-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38894-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38894-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38894-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38894-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38894-122">INPUTS</span></span>

### <span data-ttu-id="38894-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="38894-123">None</span></span>

## <span data-ttu-id="38894-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38894-124">OUTPUTS</span></span>

### <span data-ttu-id="38894-125">Microsoft. Azure. Commands. Network. models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="38894-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="38894-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38894-126">NOTES</span></span>

## <span data-ttu-id="38894-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38894-127">RELATED LINKS</span></span>
