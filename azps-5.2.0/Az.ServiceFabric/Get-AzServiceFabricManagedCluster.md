---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347818"
---
# <span data-ttu-id="a5177-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="a5177-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="a5177-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5177-102">SYNOPSIS</span></span>
<span data-ttu-id="a5177-103">Uzyskiwanie szczegółów zarządzanego zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="a5177-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="a5177-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5177-104">SYNTAX</span></span>

### <span data-ttu-id="a5177-105">BySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a5177-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5177-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a5177-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5177-107">ByName</span><span class="sxs-lookup"><span data-stu-id="a5177-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5177-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a5177-108">DESCRIPTION</span></span>
<span data-ttu-id="a5177-109">Uzyskiwanie szczegółów zarządzanego zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="a5177-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="a5177-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5177-110">EXAMPLES</span></span>

### <span data-ttu-id="a5177-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5177-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="a5177-112">Pobierz szczegóły klastra.</span><span class="sxs-lookup"><span data-stu-id="a5177-112">Get cluster details.</span></span>

### <span data-ttu-id="a5177-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a5177-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="a5177-114">Pobierz listę klastrów pod określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="a5177-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="a5177-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a5177-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="a5177-116">Pobierz listę klastrów w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a5177-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="a5177-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5177-117">PARAMETERS</span></span>

### <span data-ttu-id="a5177-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5177-118">-DefaultProfile</span></span>
<span data-ttu-id="a5177-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5177-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5177-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5177-120">-Name</span></span>
<span data-ttu-id="a5177-121">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="a5177-121">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a5177-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5177-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5177-123">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a5177-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a5177-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5177-124">CommonParameters</span></span>
<span data-ttu-id="a5177-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5177-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5177-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5177-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5177-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5177-127">INPUTS</span></span>

### <span data-ttu-id="a5177-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a5177-128">System.String</span></span>

## <span data-ttu-id="a5177-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5177-129">OUTPUTS</span></span>

### <span data-ttu-id="a5177-130">Microsoft. Azure. Commands. servicefabric. MODELES. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="a5177-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="a5177-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5177-131">NOTES</span></span>

## <span data-ttu-id="a5177-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5177-132">RELATED LINKS</span></span>
