---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: 81398d4ab62db1b8dca573dfd6beccde3be63700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872351"
---
# <span data-ttu-id="d46ec-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="d46ec-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="d46ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d46ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d46ec-103">Aktualizowanie informacji kontaktowych</span><span class="sxs-lookup"><span data-stu-id="d46ec-103">Update Contact Information</span></span>

## <span data-ttu-id="d46ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d46ec-104">SYNTAX</span></span>

### <span data-ttu-id="d46ec-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d46ec-105">ByName (Default)</span></span>
```
Set-AzPeerAsn [-Name] <String> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d46ec-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="d46ec-106">Default</span></span>
```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d46ec-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d46ec-107">DESCRIPTION</span></span>
<span data-ttu-id="d46ec-108">Umożliwia zaktualizowanie informacji kontaktowych dla PeerAsn w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d46ec-108">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="d46ec-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d46ec-109">EXAMPLES</span></span>

### <span data-ttu-id="d46ec-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d46ec-110">Example 1</span></span>
```powershell
#Get the Peer ASN object
PS C:> Get-AzPeerAsn -PeerName Contoso | Set-AzPeerAsn -Email noc1@contoso.com

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="d46ec-111">Dodaje adres e-mail do elementu równorzędnego ASN</span><span class="sxs-lookup"><span data-stu-id="d46ec-111">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="d46ec-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d46ec-112">PARAMETERS</span></span>

### <span data-ttu-id="d46ec-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d46ec-113">-AsJob</span></span>
<span data-ttu-id="d46ec-114">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="d46ec-114">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46ec-115">-DefaultProfile</span></span>
<span data-ttu-id="d46ec-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d46ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d46ec-117">-Mail</span><span class="sxs-lookup"><span data-stu-id="d46ec-117">-Email</span></span>
<span data-ttu-id="d46ec-118">Adres e-mail</span><span class="sxs-lookup"><span data-stu-id="d46ec-118">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ec-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d46ec-119">-InputObject</span></span>
<span data-ttu-id="d46ec-120">{{Fillobject opis}}</span><span class="sxs-lookup"><span data-stu-id="d46ec-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d46ec-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d46ec-121">-Name</span></span>
<span data-ttu-id="d46ec-122">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="d46ec-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ec-123">-Phone</span><span class="sxs-lookup"><span data-stu-id="d46ec-123">-Phone</span></span>
<span data-ttu-id="d46ec-124">Służb</span><span class="sxs-lookup"><span data-stu-id="d46ec-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ec-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d46ec-125">-Confirm</span></span>
<span data-ttu-id="d46ec-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d46ec-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46ec-127">-WhatIf</span></span>
<span data-ttu-id="d46ec-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d46ec-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d46ec-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d46ec-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46ec-130">CommonParameters</span></span>
<span data-ttu-id="d46ec-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d46ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46ec-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d46ec-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46ec-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d46ec-133">INPUTS</span></span>

### <span data-ttu-id="d46ec-134">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="d46ec-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="d46ec-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d46ec-135">OUTPUTS</span></span>

### <span data-ttu-id="d46ec-136">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="d46ec-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="d46ec-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d46ec-137">NOTES</span></span>

## <span data-ttu-id="d46ec-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d46ec-138">RELATED LINKS</span></span>
