---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 5f034253326f551c5b1930f6cf90a80c83ed82f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526590"
---
# <span data-ttu-id="9b6e0-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="9b6e0-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="9b6e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b6e0-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6e0-103">Pobieranie szczegółów zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b6e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b6e0-104">SYNTAX</span></span>

### <span data-ttu-id="9b6e0-105">BySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9b6e0-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b6e0-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9b6e0-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b6e0-107">ByName</span><span class="sxs-lookup"><span data-stu-id="9b6e0-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b6e0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9b6e0-108">DESCRIPTION</span></span>
<span data-ttu-id="9b6e0-109">**Dodatek Add-AzureRmServiceFabricCluster** wyświetli dane zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-109">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="9b6e0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b6e0-110">EXAMPLES</span></span>

### <span data-ttu-id="9b6e0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b6e0-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="9b6e0-112">To polecenie spowoduje pobranie szczegółów zasobu klastra dotyczących klastra.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="9b6e0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b6e0-113">PARAMETERS</span></span>

### <span data-ttu-id="9b6e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6e0-114">-DefaultProfile</span></span>
<span data-ttu-id="9b6e0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b6e0-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b6e0-116">-Name</span></span>
<span data-ttu-id="9b6e0-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-117">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b6e0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b6e0-118">-ResourceGroupName</span></span>
<span data-ttu-id="9b6e0-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b6e0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6e0-120">CommonParameters</span></span>
<span data-ttu-id="9b6e0-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6e0-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b6e0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6e0-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b6e0-123">INPUTS</span></span>

### <span data-ttu-id="9b6e0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9b6e0-124">System.String</span></span>

## <span data-ttu-id="9b6e0-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b6e0-125">OUTPUTS</span></span>

### <span data-ttu-id="9b6e0-126">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. servicefabric. MODELES. PsCluster, Microsoft. Azure. Commands. servicefabric, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9b6e0-126">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9b6e0-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b6e0-127">NOTES</span></span>

## <span data-ttu-id="9b6e0-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b6e0-128">RELATED LINKS</span></span>

