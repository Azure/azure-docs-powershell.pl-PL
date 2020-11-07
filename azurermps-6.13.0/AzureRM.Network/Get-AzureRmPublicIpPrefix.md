---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 772f0a3bb1198bf5c8d00ad8c0dd708c37c92366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716942"
---
# <span data-ttu-id="51816-101">Get-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="51816-101">Get-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="51816-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51816-102">SYNOPSIS</span></span>
<span data-ttu-id="51816-103">Pobiera publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="51816-103">Gets a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51816-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51816-104">SYNTAX</span></span>

### <span data-ttu-id="51816-105">Domyślne</span><span class="sxs-lookup"><span data-stu-id="51816-105">(Default)</span></span>
```
Get-AzureRmPublicIpPrefix [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51816-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="51816-106">GetByNameParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51816-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51816-107">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51816-108">Opis</span><span class="sxs-lookup"><span data-stu-id="51816-108">DESCRIPTION</span></span>
<span data-ttu-id="51816-109">Polecenie cmdlet **Get-AzureRmPublicIpPrefix** pobiera co najmniej jeden publiczny prefiks adresów IP w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="51816-109">The **Get-AzureRmPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="51816-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51816-110">EXAMPLES</span></span>

### <span data-ttu-id="51816-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51816-111">Example 1</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -ResourceGroupName $rgname -Name $prefixName
```

<span data-ttu-id="51816-112">To polecenie pobiera publiczny zasób prefiksu IP z $prefixName w grupie zasób $rgName</span><span class="sxs-lookup"><span data-stu-id="51816-112">This command gets a public IP prefix resource with $prefixName in resource group $rgName</span></span>

## <span data-ttu-id="51816-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51816-113">PARAMETERS</span></span>

### <span data-ttu-id="51816-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51816-114">-DefaultProfile</span></span>
<span data-ttu-id="51816-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51816-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51816-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51816-116">-Name</span></span>
<span data-ttu-id="51816-117">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="51816-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51816-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51816-118">-ResourceGroupName</span></span>
<span data-ttu-id="51816-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="51816-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51816-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51816-120">-ResourceId</span></span>
<span data-ttu-id="51816-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="51816-121">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51816-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51816-122">CommonParameters</span></span>
<span data-ttu-id="51816-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51816-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="51816-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51816-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51816-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51816-125">INPUTS</span></span>

### <span data-ttu-id="51816-126">System. String</span><span class="sxs-lookup"><span data-stu-id="51816-126">System.String</span></span>


## <span data-ttu-id="51816-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51816-127">OUTPUTS</span></span>

### <span data-ttu-id="51816-128">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="51816-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="51816-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51816-129">NOTES</span></span>

## <span data-ttu-id="51816-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51816-130">RELATED LINKS</span></span>
