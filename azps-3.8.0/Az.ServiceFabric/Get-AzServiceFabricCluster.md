---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: f35cfcbfea4bdca0b75c2048fa403712c3262e02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053422"
---
# <span data-ttu-id="be11c-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="be11c-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="be11c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be11c-102">SYNOPSIS</span></span>
<span data-ttu-id="be11c-103">Pobieranie szczegółów zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="be11c-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="be11c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be11c-104">SYNTAX</span></span>

### <span data-ttu-id="be11c-105">BySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="be11c-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be11c-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be11c-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be11c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="be11c-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be11c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="be11c-108">DESCRIPTION</span></span>
<span data-ttu-id="be11c-109">Program **Get-AzServiceFabricCluster** pobierze dane zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="be11c-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="be11c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be11c-110">EXAMPLES</span></span>

### <span data-ttu-id="be11c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="be11c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="be11c-112">To polecenie spowoduje pobranie szczegółów zasobu klastra dotyczących klastra.</span><span class="sxs-lookup"><span data-stu-id="be11c-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="be11c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be11c-113">PARAMETERS</span></span>

### <span data-ttu-id="be11c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be11c-114">-DefaultProfile</span></span>
<span data-ttu-id="be11c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="be11c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be11c-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be11c-116">-Name</span></span>
<span data-ttu-id="be11c-117">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="be11c-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="be11c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be11c-118">-ResourceGroupName</span></span>
<span data-ttu-id="be11c-119">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="be11c-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="be11c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be11c-120">CommonParameters</span></span>
<span data-ttu-id="be11c-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be11c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be11c-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be11c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be11c-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be11c-123">INPUTS</span></span>

### <span data-ttu-id="be11c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="be11c-124">System.String</span></span>

## <span data-ttu-id="be11c-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be11c-125">OUTPUTS</span></span>

### <span data-ttu-id="be11c-126">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="be11c-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="be11c-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be11c-127">NOTES</span></span>

## <span data-ttu-id="be11c-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be11c-128">RELATED LINKS</span></span>
