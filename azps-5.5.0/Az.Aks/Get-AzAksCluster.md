---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199883"
---
# <span data-ttu-id="4b167-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="4b167-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="4b167-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b167-102">SYNOPSIS</span></span>
<span data-ttu-id="4b167-103">Lista grup zarządzanych przez Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="4b167-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="4b167-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4b167-104">SYNTAX</span></span>

### <span data-ttu-id="4b167-105">ResourceGroupParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4b167-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b167-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b167-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b167-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b167-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b167-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4b167-108">DESCRIPTION</span></span>
<span data-ttu-id="4b167-109">Lista grup zarządzanych przez Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="4b167-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="4b167-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4b167-110">EXAMPLES</span></span>

### <span data-ttu-id="4b167-111">Lista wszystkich klastrów Kubernetes</span><span class="sxs-lookup"><span data-stu-id="4b167-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="4b167-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b167-112">PARAMETERS</span></span>

### <span data-ttu-id="4b167-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b167-113">-DefaultProfile</span></span>
<span data-ttu-id="4b167-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b167-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b167-115">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="4b167-115">-Id</span></span>
<span data-ttu-id="4b167-116">Identyfikator zarządzanego klastru Kubernetes</span><span class="sxs-lookup"><span data-stu-id="4b167-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="4b167-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4b167-117">-Name</span></span>
<span data-ttu-id="4b167-118">Nazwa zarządzanego klastru Kubernetes</span><span class="sxs-lookup"><span data-stu-id="4b167-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="4b167-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b167-119">-ResourceGroupName</span></span>
<span data-ttu-id="4b167-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4b167-120">Resource group name</span></span>

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

### <span data-ttu-id="4b167-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b167-121">CommonParameters</span></span>
<span data-ttu-id="4b167-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b167-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b167-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b167-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b167-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b167-124">INPUTS</span></span>

### <span data-ttu-id="4b167-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4b167-125">System.String</span></span>

## <span data-ttu-id="4b167-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4b167-126">OUTPUTS</span></span>

### <span data-ttu-id="4b167-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="4b167-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="4b167-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4b167-128">NOTES</span></span>

## <span data-ttu-id="4b167-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b167-129">RELATED LINKS</span></span>
