---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502574"
---
# <span data-ttu-id="6f521-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="6f521-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="6f521-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f521-102">SYNOPSIS</span></span>
<span data-ttu-id="6f521-103">Lista zarządzanych klastrów Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="6f521-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="6f521-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f521-104">SYNTAX</span></span>

### <span data-ttu-id="6f521-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6f521-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f521-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f521-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f521-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f521-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f521-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6f521-108">DESCRIPTION</span></span>
<span data-ttu-id="6f521-109">Lista zarządzanych klastrów Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="6f521-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="6f521-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f521-110">EXAMPLES</span></span>

### <span data-ttu-id="6f521-111">Lista wszystkich klastrów Kubernetes</span><span class="sxs-lookup"><span data-stu-id="6f521-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="6f521-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f521-112">PARAMETERS</span></span>

### <span data-ttu-id="6f521-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f521-113">-DefaultProfile</span></span>
<span data-ttu-id="6f521-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f521-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f521-115">-ID</span><span class="sxs-lookup"><span data-stu-id="6f521-115">-Id</span></span>
<span data-ttu-id="6f521-116">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="6f521-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f521-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6f521-117">-Name</span></span>
<span data-ttu-id="6f521-118">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="6f521-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f521-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f521-119">-ResourceGroupName</span></span>
<span data-ttu-id="6f521-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6f521-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f521-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f521-121">CommonParameters</span></span>
<span data-ttu-id="6f521-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f521-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f521-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f521-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f521-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f521-124">INPUTS</span></span>

### <span data-ttu-id="6f521-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6f521-125">System.String</span></span>

## <span data-ttu-id="6f521-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f521-126">OUTPUTS</span></span>

### <span data-ttu-id="6f521-127">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="6f521-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="6f521-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f521-128">NOTES</span></span>

## <span data-ttu-id="6f521-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f521-129">RELATED LINKS</span></span>
