---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f5fbef7c67676f16793b63a8448517ca24aa7e5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889310"
---
# <span data-ttu-id="2b251-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="2b251-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="2b251-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b251-102">SYNOPSIS</span></span>
<span data-ttu-id="2b251-103">Zapoznaj się z omówieniem stanu dostawcy zasobów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="2b251-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="2b251-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b251-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="2b251-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b251-105">DESCRIPTION</span></span>
<span data-ttu-id="2b251-106">Zapoznaj się z omówieniem stanu dostawcy zasobów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="2b251-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="2b251-107">Poszczególne właściwości zapewniają szczegółowe zliczanie użycia zasobów i kondycji według składników.</span><span class="sxs-lookup"><span data-stu-id="2b251-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="2b251-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b251-108">EXAMPLES</span></span>

### <span data-ttu-id="2b251-109">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="2b251-109">EXAMPLE 1</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="2b251-110">Zapoznanie się z omówieniem administratora sieci.</span><span class="sxs-lookup"><span data-stu-id="2b251-110">Get network admin overview.</span></span>

### <span data-ttu-id="2b251-111">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="2b251-111">EXAMPLE 2</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="2b251-112">Uzyskaj publiczne użycie adresu IP.</span><span class="sxs-lookup"><span data-stu-id="2b251-112">Get public ip address usage.</span></span>

## <span data-ttu-id="2b251-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b251-113">PARAMETERS</span></span>

### <span data-ttu-id="2b251-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b251-114">CommonParameters</span></span>
<span data-ttu-id="2b251-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b251-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b251-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b251-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b251-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b251-117">INPUTS</span></span>

## <span data-ttu-id="2b251-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b251-118">OUTPUTS</span></span>

### <span data-ttu-id="2b251-119">Microsoft. AzureStack. Management. Network. admin. models. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="2b251-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="2b251-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b251-120">NOTES</span></span>

## <span data-ttu-id="2b251-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b251-121">RELATED LINKS</span></span>
