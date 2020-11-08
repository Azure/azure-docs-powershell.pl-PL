---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
ms.openlocfilehash: d88ac0feab52d5f62a06981d8fa178db6dad9578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050939"
---
# <span data-ttu-id="cd70a-101">Get-AzAks</span><span class="sxs-lookup"><span data-stu-id="cd70a-101">Get-AzAks</span></span>

## <span data-ttu-id="cd70a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd70a-102">SYNOPSIS</span></span>
<span data-ttu-id="cd70a-103">Lista zarządzanych klastrów Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="cd70a-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="cd70a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd70a-104">SYNTAX</span></span>

### <span data-ttu-id="cd70a-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd70a-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd70a-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd70a-106">IdParameterSet</span></span>
```
Get-AzAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd70a-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd70a-107">NameParameterSet</span></span>
```
Get-AzAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd70a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cd70a-108">DESCRIPTION</span></span>
<span data-ttu-id="cd70a-109">Lista zarządzanych klastrów Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="cd70a-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="cd70a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd70a-110">EXAMPLES</span></span>

### <span data-ttu-id="cd70a-111">Lista wszystkich klastrów Kubernetes</span><span class="sxs-lookup"><span data-stu-id="cd70a-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzAks
```

## <span data-ttu-id="cd70a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd70a-112">PARAMETERS</span></span>

### <span data-ttu-id="cd70a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd70a-113">-DefaultProfile</span></span>
<span data-ttu-id="cd70a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd70a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd70a-115">-ID</span><span class="sxs-lookup"><span data-stu-id="cd70a-115">-Id</span></span>
<span data-ttu-id="cd70a-116">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="cd70a-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="cd70a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd70a-117">-Name</span></span>
<span data-ttu-id="cd70a-118">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="cd70a-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="cd70a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd70a-119">-ResourceGroupName</span></span>
<span data-ttu-id="cd70a-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cd70a-120">Resource group name</span></span>

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

### <span data-ttu-id="cd70a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd70a-121">CommonParameters</span></span>
<span data-ttu-id="cd70a-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd70a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd70a-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd70a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd70a-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd70a-124">INPUTS</span></span>

### <span data-ttu-id="cd70a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cd70a-125">System.String</span></span>

## <span data-ttu-id="cd70a-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd70a-126">OUTPUTS</span></span>

### <span data-ttu-id="cd70a-127">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="cd70a-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="cd70a-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd70a-128">NOTES</span></span>

## <span data-ttu-id="cd70a-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd70a-129">RELATED LINKS</span></span>
