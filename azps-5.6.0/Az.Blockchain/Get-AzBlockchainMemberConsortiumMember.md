---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: 19901a3834716e1f2b04102c4904c059fab29397
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971505"
---
# <span data-ttu-id="631c7-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="631c7-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="631c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="631c7-102">SYNOPSIS</span></span>
<span data-ttu-id="631c7-103">Wyświetla listę członków organizacji, którzy są jej członkami.</span><span class="sxs-lookup"><span data-stu-id="631c7-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="631c7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="631c7-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="631c7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="631c7-105">DESCRIPTION</span></span>
<span data-ttu-id="631c7-106">Wyświetla listę członków organizacji, którzy są jej członkami.</span><span class="sxs-lookup"><span data-stu-id="631c7-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="631c7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="631c7-107">EXAMPLES</span></span>

### <span data-ttu-id="631c7-108">Przykład 1. Lista członków tego przedsiębiorstwa.</span><span class="sxs-lookup"><span data-stu-id="631c7-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="631c7-109">To polecenie zawiera listę członków organizacji, którzy są członkami tego zespołu.</span><span class="sxs-lookup"><span data-stu-id="631c7-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="631c7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="631c7-110">PARAMETERS</span></span>

### <span data-ttu-id="631c7-111">-Wymusz na użytkownikach</span><span class="sxs-lookup"><span data-stu-id="631c7-111">-BlockchainMemberName</span></span>
<span data-ttu-id="631c7-112">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="631c7-112">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631c7-113">-DefaultProfile</span></span>
<span data-ttu-id="631c7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="631c7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631c7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="631c7-115">-ResourceGroupName</span></span>
<span data-ttu-id="631c7-116">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="631c7-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="631c7-117">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="631c7-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631c7-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="631c7-118">-SubscriptionId</span></span>
<span data-ttu-id="631c7-119">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="631c7-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="631c7-120">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="631c7-120">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631c7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631c7-121">CommonParameters</span></span>
<span data-ttu-id="631c7-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="631c7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631c7-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="631c7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631c7-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="631c7-124">INPUTS</span></span>

## <span data-ttu-id="631c7-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="631c7-125">OUTPUTS</span></span>

### <span data-ttu-id="631c7-126">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.api20180601Preview.IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="631c7-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="631c7-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="631c7-127">NOTES</span></span>

<span data-ttu-id="631c7-128">ALIASY</span><span class="sxs-lookup"><span data-stu-id="631c7-128">ALIASES</span></span>

## <span data-ttu-id="631c7-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="631c7-129">RELATED LINKS</span></span>

