---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234026"
---
# <span data-ttu-id="58c4f-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="58c4f-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="58c4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="58c4f-103">Wyświetla listę członków konsorcjum członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="58c4f-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="58c4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58c4f-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="58c4f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="58c4f-106">Wyświetla listę członków konsorcjum członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="58c4f-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="58c4f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58c4f-107">EXAMPLES</span></span>

### <span data-ttu-id="58c4f-108">Przykład 1: umożliwia wyświetlenie listy członków konsorcjum członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="58c4f-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="58c4f-109">To polecenie umożliwia wyświetlenie listy członków konsorcjum dla członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="58c4f-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="58c4f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58c4f-110">PARAMETERS</span></span>

### <span data-ttu-id="58c4f-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="58c4f-111">-BlockchainMemberName</span></span>
<span data-ttu-id="58c4f-112">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="58c4f-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="58c4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c4f-113">-DefaultProfile</span></span>
<span data-ttu-id="58c4f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58c4f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58c4f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c4f-115">-ResourceGroupName</span></span>
<span data-ttu-id="58c4f-116">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="58c4f-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="58c4f-117">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="58c4f-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="58c4f-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="58c4f-118">-SubscriptionId</span></span>
<span data-ttu-id="58c4f-119">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="58c4f-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="58c4f-120">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="58c4f-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="58c4f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c4f-121">CommonParameters</span></span>
<span data-ttu-id="58c4f-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c4f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c4f-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58c4f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c4f-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58c4f-124">INPUTS</span></span>

## <span data-ttu-id="58c4f-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58c4f-125">OUTPUTS</span></span>

### <span data-ttu-id="58c4f-126">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="58c4f-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="58c4f-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58c4f-127">NOTES</span></span>

<span data-ttu-id="58c4f-128">PISUJE</span><span class="sxs-lookup"><span data-stu-id="58c4f-128">ALIASES</span></span>

## <span data-ttu-id="58c4f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58c4f-129">RELATED LINKS</span></span>

