---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: 4eb210380feaaf101bad45b4bd0b4df26533f9e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993896"
---
# <span data-ttu-id="0e36f-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="0e36f-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="0e36f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e36f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e36f-103">Uzyskaj dostępne aliasy usługi w regionie.</span><span class="sxs-lookup"><span data-stu-id="0e36f-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="0e36f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e36f-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e36f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e36f-105">DESCRIPTION</span></span>
<span data-ttu-id="0e36f-106">Polecenie **cmdlet Get-AzAvailableServiceAlias** umożliwia pobranie wszystkich dostępnych aliasów usługi dla podsieci w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0e36f-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="0e36f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e36f-107">EXAMPLES</span></span>

### <span data-ttu-id="0e36f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e36f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="0e36f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e36f-109">PARAMETERS</span></span>

### <span data-ttu-id="0e36f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e36f-110">-DefaultProfile</span></span>
<span data-ttu-id="0e36f-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e36f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e36f-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0e36f-112">-Location</span></span>
<span data-ttu-id="0e36f-113">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="0e36f-113">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e36f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e36f-114">CommonParameters</span></span>
<span data-ttu-id="0e36f-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e36f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e36f-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e36f-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e36f-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e36f-117">INPUTS</span></span>

### <span data-ttu-id="0e36f-118">System.String</span><span class="sxs-lookup"><span data-stu-id="0e36f-118">System.String</span></span>

## <span data-ttu-id="0e36f-119">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e36f-119">OUTPUTS</span></span>

### <span data-ttu-id="0e36f-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="0e36f-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="0e36f-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e36f-121">NOTES</span></span>

## <span data-ttu-id="0e36f-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e36f-122">RELATED LINKS</span></span>
