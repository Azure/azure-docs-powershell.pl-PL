---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: acf9d604a793d4631641a87b222260d8687807cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232603"
---
# <span data-ttu-id="a9346-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="a9346-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="a9346-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9346-102">SYNOPSIS</span></span>
<span data-ttu-id="a9346-103">Uzyskaj dostęp do dostępnych aliasów usług w regionie.</span><span class="sxs-lookup"><span data-stu-id="a9346-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="a9346-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9346-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9346-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a9346-105">DESCRIPTION</span></span>
<span data-ttu-id="a9346-106">Polecenie cmdlet **Get-AzAvailableServiceAlias** umożliwia pobranie wszystkich dostępnych aliasów usługi dla podsieci w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a9346-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="a9346-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9346-107">EXAMPLES</span></span>

### <span data-ttu-id="a9346-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9346-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="a9346-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9346-109">PARAMETERS</span></span>

### <span data-ttu-id="a9346-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9346-110">-DefaultProfile</span></span>
<span data-ttu-id="a9346-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9346-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9346-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a9346-112">-Location</span></span>
<span data-ttu-id="a9346-113">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a9346-113">The location.</span></span>

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

### <span data-ttu-id="a9346-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9346-114">CommonParameters</span></span>
<span data-ttu-id="a9346-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9346-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9346-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9346-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9346-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9346-117">INPUTS</span></span>

### <span data-ttu-id="a9346-118">System. String</span><span class="sxs-lookup"><span data-stu-id="a9346-118">System.String</span></span>

## <span data-ttu-id="a9346-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9346-119">OUTPUTS</span></span>

### <span data-ttu-id="a9346-120">Microsoft. Azure. Commands. Network. models. PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="a9346-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="a9346-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9346-121">NOTES</span></span>

## <span data-ttu-id="a9346-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9346-122">RELATED LINKS</span></span>
