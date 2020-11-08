---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219504"
---
# <span data-ttu-id="16574-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="16574-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="16574-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16574-102">SYNOPSIS</span></span>
<span data-ttu-id="16574-103">Pobierz usługę Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="16574-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="16574-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16574-104">SYNTAX</span></span>

### <span data-ttu-id="16574-105">SecurityPartnerProviderNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="16574-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16574-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16574-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16574-107">Opis</span><span class="sxs-lookup"><span data-stu-id="16574-107">DESCRIPTION</span></span>
<span data-ttu-id="16574-108">Polecenie cmdlet **Get-AzSecurityPartnerProvider** pobiera platformę Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="16574-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="16574-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16574-109">EXAMPLES</span></span>

### <span data-ttu-id="16574-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="16574-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="16574-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="16574-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="16574-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16574-112">PARAMETERS</span></span>

### <span data-ttu-id="16574-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16574-113">-DefaultProfile</span></span>
<span data-ttu-id="16574-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16574-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16574-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="16574-115">-Name</span></span>
<span data-ttu-id="16574-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="16574-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16574-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16574-117">-ResourceGroupName</span></span>
<span data-ttu-id="16574-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="16574-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16574-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16574-119">-ResourceId</span></span>
<span data-ttu-id="16574-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="16574-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16574-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16574-121">CommonParameters</span></span>
<span data-ttu-id="16574-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16574-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16574-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16574-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16574-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16574-124">INPUTS</span></span>

### <span data-ttu-id="16574-125">System. String</span><span class="sxs-lookup"><span data-stu-id="16574-125">System.String</span></span>

## <span data-ttu-id="16574-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16574-126">OUTPUTS</span></span>

### <span data-ttu-id="16574-127">Microsoft. Azure. Commands. Network. models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="16574-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="16574-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16574-128">NOTES</span></span>

## <span data-ttu-id="16574-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16574-129">RELATED LINKS</span></span>
