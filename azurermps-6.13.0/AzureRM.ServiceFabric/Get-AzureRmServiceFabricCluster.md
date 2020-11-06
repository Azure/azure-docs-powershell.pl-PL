---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 93240fe3deddbe5b6f8fb20d644a0e685cfdda11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550215"
---
# <span data-ttu-id="326e8-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="326e8-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="326e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="326e8-102">SYNOPSIS</span></span>
<span data-ttu-id="326e8-103">Pobieranie szczegółów zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="326e8-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="326e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="326e8-104">SYNTAX</span></span>

### <span data-ttu-id="326e8-105">BySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="326e8-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="326e8-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="326e8-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="326e8-107">ByName</span><span class="sxs-lookup"><span data-stu-id="326e8-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="326e8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="326e8-108">DESCRIPTION</span></span>
<span data-ttu-id="326e8-109">Program **Get-AzureRmServiceFabricCluster** pobierze dane zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="326e8-109">The **Get-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="326e8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="326e8-110">EXAMPLES</span></span>

### <span data-ttu-id="326e8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="326e8-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="326e8-112">To polecenie spowoduje pobranie szczegółów zasobu klastra dotyczących klastra.</span><span class="sxs-lookup"><span data-stu-id="326e8-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="326e8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="326e8-113">PARAMETERS</span></span>

### <span data-ttu-id="326e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="326e8-114">-DefaultProfile</span></span>
<span data-ttu-id="326e8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="326e8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="326e8-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="326e8-116">-Name</span></span>
<span data-ttu-id="326e8-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="326e8-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="326e8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="326e8-118">-ResourceGroupName</span></span>
<span data-ttu-id="326e8-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="326e8-119">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="326e8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326e8-120">CommonParameters</span></span>
<span data-ttu-id="326e8-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="326e8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326e8-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="326e8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326e8-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="326e8-123">INPUTS</span></span>

### <span data-ttu-id="326e8-124">System. String</span><span class="sxs-lookup"><span data-stu-id="326e8-124">System.String</span></span>

## <span data-ttu-id="326e8-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="326e8-125">OUTPUTS</span></span>

### <span data-ttu-id="326e8-126">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="326e8-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="326e8-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="326e8-127">NOTES</span></span>

## <span data-ttu-id="326e8-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="326e8-128">RELATED LINKS</span></span>
