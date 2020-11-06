---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/get-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
ms.openlocfilehash: ee8420a8869e1056dc0ee3d942b811c3f70d545d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549028"
---
# <span data-ttu-id="6ad32-101">Get-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="6ad32-101">Get-AzureRmAks</span></span>

## <span data-ttu-id="6ad32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ad32-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad32-103">Lista zarządzanych klastrów Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="6ad32-103">List Kubernetes managed clusters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ad32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ad32-104">SYNTAX</span></span>

### <span data-ttu-id="6ad32-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6ad32-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ad32-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ad32-106">IdParameterSet</span></span>
```
Get-AzureRmAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ad32-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ad32-107">NameParameterSet</span></span>
```
Get-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ad32-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6ad32-108">DESCRIPTION</span></span>
<span data-ttu-id="6ad32-109">Lista zarządzanych klastrów Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="6ad32-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="6ad32-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ad32-110">EXAMPLES</span></span>

### <span data-ttu-id="6ad32-111">Lista wszystkich klastrów Kubernetes</span><span class="sxs-lookup"><span data-stu-id="6ad32-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzureRmAks
```

## <span data-ttu-id="6ad32-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ad32-112">PARAMETERS</span></span>

### <span data-ttu-id="6ad32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad32-113">-DefaultProfile</span></span>
<span data-ttu-id="6ad32-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad32-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ad32-115">-ID</span><span class="sxs-lookup"><span data-stu-id="6ad32-115">-Id</span></span>
<span data-ttu-id="6ad32-116">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="6ad32-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad32-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ad32-117">-Name</span></span>
<span data-ttu-id="6ad32-118">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="6ad32-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad32-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad32-119">-ResourceGroupName</span></span>
<span data-ttu-id="6ad32-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6ad32-120">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad32-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad32-121">CommonParameters</span></span>
<span data-ttu-id="6ad32-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad32-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad32-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad32-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad32-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ad32-124">INPUTS</span></span>

### <span data-ttu-id="6ad32-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6ad32-125">System.String</span></span>

## <span data-ttu-id="6ad32-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ad32-126">OUTPUTS</span></span>

### <span data-ttu-id="6ad32-127">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="6ad32-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="6ad32-128">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. AKS. MODELES. PSKubernetesCluster, Microsoft. Azure. Commands. AKS, Version = 0.0.0.0, Culture = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6ad32-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster, Microsoft.Azure.Commands.Aks, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6ad32-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ad32-129">NOTES</span></span>

## <span data-ttu-id="6ad32-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ad32-130">RELATED LINKS</span></span>
