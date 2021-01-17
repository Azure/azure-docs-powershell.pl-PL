---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384629"
---
# <span data-ttu-id="8747e-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="8747e-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="8747e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8747e-102">SYNOPSIS</span></span>
<span data-ttu-id="8747e-103">Aktualizowanie informacji kontaktowych</span><span class="sxs-lookup"><span data-stu-id="8747e-103">Update Contact Information</span></span>

## <span data-ttu-id="8747e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8747e-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8747e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8747e-105">DESCRIPTION</span></span>
<span data-ttu-id="8747e-106">Umożliwia zaktualizowanie informacji kontaktowych dla PeerAsn w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8747e-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="8747e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8747e-107">EXAMPLES</span></span>

### <span data-ttu-id="8747e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8747e-108">Example 1</span></span>
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

<span data-ttu-id="8747e-109">Dodaje adres e-mail do elementu równorzędnego ASN</span><span class="sxs-lookup"><span data-stu-id="8747e-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="8747e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8747e-110">PARAMETERS</span></span>

### <span data-ttu-id="8747e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8747e-111">-AsJob</span></span>
<span data-ttu-id="8747e-112">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="8747e-112">Run in the background.</span></span>

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

### <span data-ttu-id="8747e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8747e-113">-DefaultProfile</span></span>
<span data-ttu-id="8747e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8747e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8747e-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8747e-115">-InputObject</span></span>
<span data-ttu-id="8747e-116">{{Fillobject opis}}</span><span class="sxs-lookup"><span data-stu-id="8747e-116">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8747e-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8747e-117">-Confirm</span></span>
<span data-ttu-id="8747e-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8747e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8747e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8747e-119">-WhatIf</span></span>
<span data-ttu-id="8747e-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8747e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8747e-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8747e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8747e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8747e-122">CommonParameters</span></span>
<span data-ttu-id="8747e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8747e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8747e-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8747e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8747e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8747e-125">INPUTS</span></span>

### <span data-ttu-id="8747e-126">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="8747e-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="8747e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8747e-127">OUTPUTS</span></span>

### <span data-ttu-id="8747e-128">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="8747e-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="8747e-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8747e-129">NOTES</span></span>

## <span data-ttu-id="8747e-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8747e-130">RELATED LINKS</span></span>
