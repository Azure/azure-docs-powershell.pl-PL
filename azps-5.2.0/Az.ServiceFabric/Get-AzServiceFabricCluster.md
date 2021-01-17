---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347821"
---
# <span data-ttu-id="c6987-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c6987-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="c6987-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6987-102">SYNOPSIS</span></span>
<span data-ttu-id="c6987-103">Pobieranie szczegółów zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="c6987-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="c6987-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6987-104">SYNTAX</span></span>

### <span data-ttu-id="c6987-105">BySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c6987-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6987-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c6987-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6987-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c6987-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6987-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c6987-108">DESCRIPTION</span></span>
<span data-ttu-id="c6987-109">Program **Get-AzServiceFabricCluster** pobierze dane zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="c6987-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="c6987-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6987-110">EXAMPLES</span></span>

### <span data-ttu-id="c6987-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c6987-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="c6987-112">To polecenie spowoduje pobranie szczegółów zasobu klastra dotyczących klastra.</span><span class="sxs-lookup"><span data-stu-id="c6987-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="c6987-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6987-113">PARAMETERS</span></span>

### <span data-ttu-id="c6987-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6987-114">-DefaultProfile</span></span>
<span data-ttu-id="c6987-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6987-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6987-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c6987-116">-Name</span></span>
<span data-ttu-id="c6987-117">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="c6987-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="c6987-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6987-118">-ResourceGroupName</span></span>
<span data-ttu-id="c6987-119">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6987-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c6987-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6987-120">CommonParameters</span></span>
<span data-ttu-id="c6987-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6987-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6987-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6987-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6987-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6987-123">INPUTS</span></span>

### <span data-ttu-id="c6987-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c6987-124">System.String</span></span>

## <span data-ttu-id="c6987-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6987-125">OUTPUTS</span></span>

### <span data-ttu-id="c6987-126">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="c6987-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c6987-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6987-127">NOTES</span></span>

## <span data-ttu-id="c6987-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6987-128">RELATED LINKS</span></span>
